<template>
    <v-app-bar app color="primary" dark>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>
        <img class="logo" :src="require('../assets/logo.svg')" alt="logo" />
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text to="/">Hjem</v-btn>
      <v-btn text to="/about">Om mig</v-btn>
      <v-btn text to="/projects">Projekter</v-btn>
      <v-btn text href="../assets/CV Shahad.pdf" target="_blank">CV</v-btn>
      <v-btn text to="/contact">Kontakt</v-btn>
  
      <v-navigation-drawer v-model="drawer" app right temporary>
        <v-list>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <router-link to="/">Hjem</router-link>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <router-link to="/about">Om mig</router-link>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <router-link to="/projects">Projekter</router-link>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <a href="../assets/CV Shahad.pdf" target="_blank">CV</a>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <router-link to="/contact">Kontakt</router-link>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
    </v-app-bar>
  </template>
  
  <script>
  export default {
    data() {
      return {
        drawer: false,
      };
    },
  };
  </script>
  
  <style scoped>
  .logo {
    height: 50px;
  }
  </style>