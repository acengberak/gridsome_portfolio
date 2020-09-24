<template>
  <div>
    <section>
      <v-container class="webdevelopment-section">
        <v-row>
          <v-col>
            <h1>{{ title.name }}</h1>
          </v-col>
        </v-row>
        <v-row class="justify-space-around mb-8 mt-4 mx-auto">
          <v-col v-for="project in projects" :key="project.name" cols="12" sm="3">
            <v-hover>
              <template v-slot="{ hover }">
                <v-card class="transition-swing" max-width="300" shaped :elevation="hover ? 24 : 6" min-height="100%">
                  <v-img class="white--text align-end" height="200px" :src="project.image">                
                  </v-img>
                  <v-card-title>{{ project.name }}</v-card-title>
                  <v-card-text class="text--primary">
                    <div>{{ truncate(project.description) }}</div>
                  </v-card-text>

                  <v-card-actions>
                    <v-btn color="orange" text :href="project.github" target="_blank">Github Repo</v-btn>
                    <v-btn color="orange" text :href="project.website" target="_blank">Website</v-btn>
                  </v-card-actions>
                </v-card>
              </template>
            </v-hover>
          </v-col>
        </v-row>
      </v-container>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: {
        name: "Web Development",
      },
      projects: [
        {
          name: "Boombastic",
          github: "https://youtu.be/KzZEY6F9z6I",
          website: 'https://boombastic.id/id',
          description:
            "Boombastic is a snack product made from selected cassava, unlike other cassava, our cassava wedges cutting is Crispy on the outside, soft and tasty on the inside with varieties of unique flavors. ",
          image:
            "https://i.gyazo.com/4694dab1f6545e7d737aa5ae810ef829.jpg",
        },
      ],
    };
  },
  methods: {
      truncate(str) {
          if (str.length > 40) {
              return str.slice(0, 39) + '...'
          }
          return str
      }
  },
};
</script>

<style scoped>
  .webdevelopment-section {
    background-color: #fcf9ec;
  }

  .webdevelopment-section h1 {
    color: #12D3CF;
  }

  .v-card__title {
    color: #67EACA;
  }

  .v-image {
    -webkit-filter: grayscale(100%);
    -moz-filter: grayscale(100%);
    filter: grayscale(100%);
    transition: all 0.5s ease;
  }
  .v-image:hover {
    -webkit-filter: grayscale(0%);
    -moz-filter: grayscale(0%);
    filter: grayscale(0%);
  }
</style>