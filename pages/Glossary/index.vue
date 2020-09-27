<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <h2>Glossary</h2>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <v-expansion-panels flat>
          <v-expansion-panel
            v-for="(item, i) in items"
            :key="i"
          >
            <v-expansion-panel-header>{{item.title}}</v-expansion-panel-header>
            <v-expansion-panel-content>

              <v-list>
                <v-list-item v-if="isLoading">
                  <v-list-item-content>
                    Loading...
                  </v-list-item-content>
                </v-list-item>
                <v-list-item-group v-else>
                  <v-list-item
                    v-for="(item, i) in item.posts"
                    :key="i"
                  >
                    <v-list-item-content>
                      <v-list-item-title>
                        <nuxt-link :to="item.path" class="text-decoration-none">
                          {{item.title}}
                        </nuxt-link>
                      </v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                </v-list-item-group>
              </v-list>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: "Glossary",
    data() {
      return {
        allPosts: [],
        items: {},
        isLoading: false
      }
    },
    beforeMount() {
      let char;
      for (let i = 65; i <= 90; i++) {
        char = String.fromCharCode(i);
        this.items[char] = {
          title: char,
          posts: []
        };
      }
      this.items["#"] = {
        title: "#",
        posts: []
      }
    },
    async mounted() {
      this.isLoading = true;
      this.allPosts = await this.$content('Glossary')
        .only(['title', 'path'])
        .sortBy('title', 'asc')
        .fetch();

      this.allPosts.forEach(post => {
        let firstChar = post.title.charAt(0).toUpperCase();
        let charCode = firstChar.charCodeAt(0);
        if (charCode < 65 && charCode > 90) {
          firstChar = "#";
        }
        this.items[firstChar].posts.push({
          title: post.title,
          path: post.path
        });
      })
      this.isLoading = false;
    },
  }
</script>

<style scoped>

</style>
