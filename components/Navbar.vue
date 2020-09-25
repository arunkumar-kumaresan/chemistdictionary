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
              ></v-text-field>
          </v-toolbar>
          <v-list class="mx-auto">
            Waiting to show search results!
          </v-list>
        </v-card>
      </v-dialog>
    </v-app-bar>
  </div>
</template>

<script>
  export default {
    name: "Navbar",
    data() {
      return {
        drawer: false,
        dialog: false,
        notifications: false,
        sound: true,
        widgets: false,
        items: [
          {title: 'Home', icon: 'mdi-home', path: '/'},
          {title: 'Glossary', icon: 'mdi-bookshelf', path: '/Glossary'},
          {title: 'Elements', icon: 'mdi-fire', path: '/Elements'},
          {title: 'Periodic Table', icon: 'mdi-periodic-table', path: '/PeriodicTable'},
          {title: 'Blog', icon: 'mdi-bookshelf', path: '/Blog'},
          {title: 'About Us', icon: 'mdi-account-group', path: '/AboutUs'},
        ]
      }
    }
  }
</script>

<style scoped>

</style>
