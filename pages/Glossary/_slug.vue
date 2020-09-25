<template>
  <v-container>
    <v-row>
      <v-col class="px-10">
        <h2 class="pb-3">{{doc.title}}</h2>
        <v-divider></v-divider>
      </v-col>
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
      async asyncData({ $content, params }) {
        const doc = await $content('Glossary', params.slug).fetch();
        return { doc };
      }
    }
</script>

<style scoped>

</style>
