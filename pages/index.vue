<template>
  <v-container class="py-0">
    <v-row class="mx-5">
      <v-col class="pa-0">
      <h2>Topics</h2>
      </v-col>
    </v-row>
    <v-row dense>
      <v-col cols="12">
      <v-slide-group>
        <v-slide-item
          class="ma-3"
          v-for="(topics, index) in topics"
          :key="index"
        >
      <v-card
        max-width="250"
        class="rounded-lg"
        disabled
      >
        <v-img
          class="align-end font-weight-bold"
          height="125"
          :src="topics.image"
        >
        </v-img>
        <v-card-title class="subtitle-1 font-weight-medium">{{topics.title}}</v-card-title>
        <v-card-text class="caption">
          <div>{{topics.excerpt}}</div>
        </v-card-text>

        <v-card-actions>
          <v-btn
            color="primary"
            text
            disabled
          >
            Coming Soon
          </v-btn>
        </v-card-actions>
      </v-card>
        </v-slide-item>
      </v-slide-group>
      </v-col>
    </v-row>
    <v-row dense>
      <v-col>
        <div class="d-flex flex-column flex-sm-row justify-center">
        <v-card
          class="mx-4 rounded-lg mb-4"
          max-width="300"
        >
          <v-card-text>
            <div>Word of the Day</div>
            <p class="headline text--primary">
              {{wordToday.title}}
            </p>
            <p>Definition</p>
            <div class="text--primary">
              {{wordToday.excerpt}}
            </div>
          </v-card-text>
          <v-card-actions>
            <v-btn
              text
              color="primary"
            >
              <nuxt-link :to="wordToday.path" class="text-decoration-none">
              Learn More
              </nuxt-link>
            </v-btn>
          </v-card-actions>
        </v-card>
        <v-card
          class="mx-4 rounded-lg mb-4"
          max-width="300"
        >
          <v-card-text>
            <div>Element of the Day</div>
            <p class="headline text--primary">
              {{elementToday.title}}
            </p>
            <div class="text--primary">
              {{elementToday.excerpt}}
            </div>
          </v-card-text>
          <v-card-actions>
            <v-btn
              text
              color="primary"
            >
              <nuxt-link :to="elementToday.path" class="text-decoration-none">
                Learn More
              </nuxt-link>
            </v-btn>
          </v-card-actions>
        </v-card>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    data() {
      return {
        topics: [
          {
            title: "The Solid State",
            excerpt: "The vast majority of solid substances like high temperature...",
            image: "../solid-state.jpg"
          },
          {
            title: "Solutions",
            excerpt: "Almost all processes in body occur in some kind of liquid solutions.",
            image: "../solutions.jpg"
          },
          {
            title: "Electrochemistry",
            excerpt: "Chemical reactions can be used to produce electrical energy...",
            image: "../electrochemistry.jpg"
          },
          {
            title: "Chemical Kinetics",
            excerpt: "Chemical Kinetics helps us to understand how chemical reactions...",
            image: "../chemical-kinetics.jpg"
          },
          {
            title: "Surface Chemistry",
            excerpt: "Some of the most important chemicals are produced industrially...",
            image: "../surface-chemistry.jpg"
          },
          {
            title: "Isolation of Elements",
            excerpt: "Thermodynamics illustrates why only a certain reducing element...",
            image: "../minerals.jpg"
          },
          {
            title: "The p-Block Elements",
            excerpt: "Diversity in chemistry is the hallmark of p–block elements...",
            image: "../sky.jpg"
          },
          {
            title: "The d-and f-Block Elements",
            excerpt: "Iron, copper, silver and gold are among the transition...",
            image: "../coins.jpg"
          },
          {
            title: "Coordination Compounds",
            excerpt: "Coordination Compounds are the backbone of modern inorganic...",
            image: "../basic-chemistry.jpg"
          }
        ],
        wordToday: {
          title: "Acid",
          excerpt: "An acid is a molecule or ion capable of donating a proton (hydrogen ion H+) or, alternatively, capable of forming a covalent bond with an electron pair.",
          path: "/Glossary/acid"
        },
        elementToday: {
          title: "Hydrogen",
          excerpt: "An acid is a molecule or ion capable of donating a proton (hydrogen ion H+) or, alternatively, capable of forming a covalent bond with an electron pair.",
          path: "/Element/hydrogen"
        }
      }
    }
  }
</script>
