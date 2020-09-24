<template>
  <v-app>
    <!-- <v-card
      height="400"
      width="256"
      class="mx-auto"
    > -->
      <v-navigation-drawer width="300"
        
        fixed 
        permanent>
        <v-list-item>
          <!-- <v-list-item-avatar>
              <img src="https://randomuser.me/api/portraits/men/81.jpg">
          </v-list-item-avatar> -->
          <v-list-item-content>
            <v-list-item-title class="title">
              Adityo Hariyudo
            </v-list-item-title>
            <v-list-item-subtitle>
              Motion Graphic & Fullstack Developer
            </v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>

        <v-list
          dense
          nav
        >
          <v-list-item
            v-for="item in items"
            :key="item.title"
            link
          >
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
    <!-- </v-card> -->
      <v-main>
          <slot/> 
      </v-main>  
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      items: [
          { title: 'About', icon: 'mdi-account-box-outline' },
          { title: 'Projects', icon: 'mdi-application-settings' },
          { title: 'Education & Experience', icon: 'mdi-school-outline' },
          { title: 'Contact', icon: 'mdi-human-greeting-proximity' },
        ],
      right: null,
    }
  },
}
</script>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
  
 .v-application--wrap {
   flex-direction: row;
 }
 .v-main {
   flex: 1 0;
   margin-left: 300px;
   background-color: #FCF9EC;
 }

</style>
