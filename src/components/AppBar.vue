<template>
  <v-app-bar
    class="app-bar"
    color="primary"
    dark
    height="64"
    prominent
  >
    <v-app-bar-nav-icon @click="drawer = !drawer" />
    <v-toolbar-title>Car Cherry</v-toolbar-title>
    <v-spacer />
  </v-app-bar>
  <v-navigation-drawer
    v-model="drawer"
    temporary
  >
    <v-list>
      <v-list-item
        prepend-icon="mdi-home"
        title="Home"
        to="/"
      />
      <v-list-item
        prepend-icon="mdi-car"
        title="Autos"
        to="/cars"
      />
      <v-list-item
        prepend-icon="mdi-map-marker-path"
        title="Fahrten"
        to="/trips"
      />
    </v-list>
  </v-navigation-drawer>
</template>

<script setup lang="ts">
  import { ref } from 'vue'

  const drawer = ref(false)
</script>
