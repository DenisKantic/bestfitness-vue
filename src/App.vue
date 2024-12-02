<template>
  <v-app style="margin: 0; height: 100vh; background-color: coral;">
    <Navbar />
    <HelloWorld />
    <v-spacer />
    <HelloWorld />
    <v-main />
  </v-app>
</template>

<script lang="ts" setup>
  import Navbar from "@/components/navigation_bar.vue"
  import HelloWorld from "./components/HelloWorld.vue";
</script>
