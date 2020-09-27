<template>
  <div>
    <v-navigation-drawer v-model="drawer" :permanent="$vuetify.breakpoint.mdAndUp" app floating>
      <v-list-item class="ma-5">
        <v-img src="../wordmark.png" alt="Chemist Dictionary"></v-img>
      </v-list-item>

      <v-list dense nav class="pt-3">
        <v-list-item v-for="item in items" :key="item.title" router :to="item.path" >
          <v-list-item-avatar>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-avatar>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar flat app class="secondary" height="96">
      <v-app-bar-nav-icon @click="drawer = !drawer" v-show="$vuetify.breakpoint.smAndDown"></v-app-bar-nav-icon>
      <v-toolbar-title><v-img src="../wordmark.png" alt="Chemist Dictionary" v-show="$vuetify.breakpoint.smAndDown" width="175" max-height="45" contain></v-img>
      </v-toolbar-title>
      <v-text-field
        solo
        flat
        hide-details
        rounded
        clearable
        dense
        label="Search"
        prepend-inner-icon="mdi-magnify"
        class="px-3 shrink"
        v-show="$vuetify.breakpoint.mdAndUp"
        v-model="searchQuery"
        @keyup="submitSearch"
        @focus="showResult"
        @focusout="hideResult"
      ></v-text-field>
      <v-spacer></v-spacer>
      <v-btn
        icon
        @click.stop="dialog = true"
      >
        <v-icon v-show="$vuetify.breakpoint.smAndDown">
          mdi-magnify
        </v-icon>
      </v-btn>
      <div class="searchResult" v-show="isResult">
        <div class="card">
          <div class="card-content">
            <nuxt-link  :to="article.path" v-for="article in articles" v-bind:key="article.slug" >
              <div class="content" @click="hideResult">
                {{ article.title }}
              </div>
            </nuxt-link>
          </div>
        </div>
      </div>

      <v-dialog v-model="dialog" fullscreen hide-overlay transition="dialog-top-transition">
        <v-card>
          <v-toolbar flat height="96">
            <v-btn icon @click="dialog = false">
              <v-icon>mdi-arrow-left</v-icon>
            </v-btn>
              <v-text-field
                solo
                outlined
                flat
                hide-details
                clearable
                dense
                label="Search"
                v-show="$vuetify.breakpoint.smAndDown"
                v-model="searchQuery"
                @keyup="submitSearch"
                @focus="showResult"
                @focusout="hideResult"
              ></v-text-field>
          </v-toolbar>
          <v-list class="mx-auto">
            <nuxt-link  :to="article.path" v-for="article in articles" v-bind:key="article.slug" >
              <div class="content" @click="hideResult">
                {{ article.title }}
              </div>
            </nuxt-link>
          </v-list>
        </v-card>
      </v-dialog>
    </v-app-bar>
  </div>
</template>

<script>
  const sanitizeHtml = require('sanitize-html');

  export default {
    name: "Navbar",
    data() {
      return {
        searchQuery: '',
        isResult: false,
        articles: [],
        drawer: false,
        dialog: false,
        items: [
          {title: 'Home', icon: 'mdi-home', path: '/'},
          {title: 'Glossary', icon: 'mdi-bookshelf', path: '/Glossary'},
          {title: 'Elements', icon: 'mdi-fire', path: '/Elements'},
          {title: 'Periodic Table', icon: 'mdi-periodic-table', path: '/PeriodicTable'},
          {title: 'Blog', icon: 'mdi-bookshelf', path: '/Blog'},
          {title: 'About Us', icon: 'mdi-account-group', path: '/AboutUs'},
        ]
      }
    },
    methods: {
      submitSearch: async function () {
        if (this.searchQuery.trim().length <= 2) {
          this.isResult = false;
          this.articles = [];
        } else {
          let sanitizedHTML = sanitizeHtml(this.searchQuery, {
            allowedTags: [],
            allowedAttributes: {}
          });
          const articles = await this.$content('Glossary')
            .search('title', sanitizedHTML.trim()).fetch();

          console.log(articles);
          this.isResult = !!articles.length;
          this.articles = articles;
        }
      },
      hideResult: function () {
        setTimeout(() => this.isResult = false, 200);
      },
      showResult: function () {
        if (!this.isResult) {
          this.submitSearch();
        }
      }
    }
  }
</script>

<style scoped>

</style>
