<template>
  <v-container>
    <v-row
      dense
      v-show="$vuetify.breakpoint.smAndDown"
    >
      <v-col>
        <nuxt-link to="/Glossary" class="text-decoration-none">
          <v-btn icon>
            <v-icon>mdi-arrow-left</v-icon>
          </v-btn>
        </nuxt-link>
      </v-col>
    </v-row>
    <v-row>
        <v-col class="pl-5">
        <h2>{{doc.title}}</h2>
          <p class="caption">{{ formatDate(doc.updatedAt) }}</p>
      </v-col>
    </v-row>
    <v-row>
      <v-divider></v-divider>
    </v-row>
    <v-row>
      <v-col class="px-10">
        <nuxt-content :document="doc"/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
    export default {
      layout: 'PostLayout',
      async asyncData({ $content, params }) {
        const doc = await $content('Glossary', params.slug).fetch();
        return { doc };
      },
      methods: {
        formatDate(date) {
          const options = { year: 'numeric', month: 'long', day: 'numeric' }
          return new Date(date).toLocaleDateString('en', options)
        }
      }
    }
</script>

<style scoped>

</style>
