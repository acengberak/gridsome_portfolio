<template>
  <div>
    <section id="about">
      <v-container>
        <v-row>
          <v-col sm="4">
            <v-card class="mx-auto" max-width="434" tile>
              <v-img g-image
                height="100%"
                src="https://images.pexels.com/photos/4827/nature-forest-trees-fog.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"
              >
                <v-row align="end" class="fill-height">
                  <v-col align-self="start" class="pa-0" cols="12">
                    <v-avatar class="profile" color="grey" size="230" tile>
                      <v-img
                        src="https://scontent.fcgk10-1.fna.fbcdn.net/v/t31.0-8/885416_10151358831298471_476540010_o.jpg?_nc_cat=104&_nc_sid=de6eea&_nc_ohc=JSTiJSHAdQkAX-4BArn&_nc_ht=scontent.fcgk10-1.fna&oh=5eb983ca861b201b29115dfd124bfb53&oe=5F8FEF19"
                      ></v-img>
                    </v-avatar>
                  </v-col>
                  <v-col class="py-0">
                    <v-list-item color="rgba(0, 0, 0, .4)" dark>
                      <v-list-item-content>
                        <v-list-item-title class="title"
                          >Adityo Hariyudo</v-list-item-title
                        >
                        <v-list-item-subtitle
                          >Motion graphic & Web developers</v-list-item-subtitle
                        >
                      </v-list-item-content>
                    </v-list-item>
                  </v-col>
                </v-row>
              </v-img>
            </v-card>
            
          </v-col>
          <v-col sm="6" class="d-flex flex-column justify-center">
            <h1>Hi, I'm Adityo.</h1>
            <div>
              <p>
                I'm Motion Graphic who works as 2D & 3D Motion graphics from
                Jakarta. I love writing code, and web development.
              </p>
              <p>
                I'm open for freelance motion graphics and web development
                opportunities right now. Please contact me at
                <strong>adit.goyo@gmail.com</strong>
              </p>

              <v-btn
                class="mr-3"
                :elevation="1"
                rounded
                color="primary"
                text
                :href="youtube.link"
                target="_blank"
                ><v-icon color="red" large>mdi-youtube</v-icon> &nbsp
                {{ youtube.name }}
              </v-btn>

              <v-btn
                :elevation="1"
                rounded
                color="primary"
                text
                :href="github.link"
                target="_blank"
                ><v-icon color="red" large>mdi-github</v-icon> &nbsp
                {{ github.name }}
              </v-btn>
            </div>
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
      youtube: {
        name: "Channel",
        link:
          "https://www.youtube.com/playlist?list=PLxMGAUZ5iKSZMaEeBCd6kWnba9h2loXAJ",
      },
      github: {
        name: "Github",
        link: "https://github.com/acengberak",
      },
    };
  },
};
</script>

<style scoped>

</style>