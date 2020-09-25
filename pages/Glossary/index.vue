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
            v-for="(item,i) in items"
            :key="i"
          >
            <v-expansion-panel-header>{{item.title}}</v-expansion-panel-header>
            <v-expansion-panel-content>
              <v-list>
                <v-list-item-group>
                  <v-list-item
                    v-for="(item, i) in item.items"
                    :key="i"
                  >
                    <v-list-item-content>
                      <v-list-item-title>
                        <nuxt-link :to="item.path">
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
        items: [
          {
            title: "A",
            items: [
              {title: "Acid", path: "/Glossary/acid"},
              {title: "Actinides", path: "/Glossary/actinides"},
              {title: "Alcohol", path: "/Glossary/alcohol"},
              ]
          },
          {
            title: "B",
            items: [
              {title: "Acid", path: "/Glossary/acid"}
            ]
          },
          {
            title: "C",
            items: [
              {title: "Acid", path: "/Glossary/acid"}
            ]
          },
          {
            title: "D",
            items: [
              {title: "Acid", path: "/Glossary/acid"}
            ]
          },
        ]
      }
    }
  }
</script>

<style scoped>

</style>
