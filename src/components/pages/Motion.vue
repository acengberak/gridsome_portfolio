<template>
  <div>
    <section>
      <v-container class="motion-section">
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
                    <v-btn color="orange" text :href="project.yTube" target="_blank">Watch!!</v-btn>
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
        name: "Motion Graphic",
      },
      projects: [
        {
          name: "Gong Xi Fat Choy 2019",
          yTube: "https://youtu.be/KzZEY6F9z6I",
          description:
            "PT. Prisma Harapan Indent LED Animation for Lunar Year @Semanggi",
          image:
            "https://i.gyazo.com/6ee45e4644fdf5050e2034bf8aaab6aa.png",
        },
        {
          name: "Vesak Day",
          yTube: "https://youtu.be/lOJup4G7f70",
          description:
            "PT. Prisma Harapan Indent LED Animation for Vesak Day @Semanggi",
          image:
            "https://i.gyazo.com/86f0a7f0c1baa74ad71f95e5ebc74e57.jpg",
        },
        {
          name: "Unreal Engine CSGO",
          yTube: "https://youtu.be/I63yXEsqND8",
          description: "I've made this 3d movie using Unreal Engine 4, It's really put a lots a work from x to y",
          image:
            "https://i.gyazo.com/c223249a586f454eb92a4d4478c74e3f.jpg",
        },
        {
          name: "Cornerstone",
          yTube: "https://youtu.be/rDKjdktCm6E",
          description: "Cornerstone is a group that has subsidiaries, among others, 23 Paskal shopping center, Beachwalk Bali, Fx Sudirman, and Park 23 entertainment center.",
          image:
            "https://i.gyazo.com/1efbd112e7589929be0e55c230e03b27.jpg",
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
  .motion-section {
    background-color: #fcf9ec;
  }

  h1 {
    color: #12D3CF;
  }

  .v-card__title {
    color: #67EACA;
  }

  .v-image {
   -webkit-filter: grayscale(80%);
   -moz-filter: grayscale(80%);
   filter: grayscale(80%);
   transition: all 0.5s ease;
  }
  .v-image:hover {
   -webkit-filter: grayscale(0%);
   -moz-filter: grayscale(0%);
   filter: grayscale(0%);
  }

</style>