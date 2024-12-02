<template>
  <v-app style="margin: 0;">
    <Navbar />
    <FirstPage />
    <AboutUs />
    <v-main />
  </v-app>
</template>

<script lang="ts" setup>
  import Navbar from "@/components/navigation_bar.vue"
  import FirstPage from "./components/first_page.vue";
  import AboutUs from "./components/about_us.vue";
</script>
