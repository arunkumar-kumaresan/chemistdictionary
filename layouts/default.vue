<template>
  <v-app>
    <Navbar/>
    <v-main class="secondary">
      <nuxt/>
    </v-main>
    <v-footer app>
      <!-- -->
    </v-footer>
  </v-app>
</template>

<script>
  import Navbar from "~/components/Navbar";

  export default {
    components: {Navbar},
    data() {
      return {}
    }
  }
</script>
