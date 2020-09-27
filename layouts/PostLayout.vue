<template>
  <v-app>
    <Navbar
      v-if="$vuetify.breakpoint.mdAndUp"
    />
    <v-main class="secondary">
      <nuxt/>
    </v-main>
    <v-footer app>
      <!-- -->
    </v-footer>
  </v-app>
</template>

<script>
    export default {
        name: "PostLayout"
    }
</script>
