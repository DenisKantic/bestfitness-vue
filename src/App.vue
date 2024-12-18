<template>
  <v-app style="margin: 0; background-color: #1f1f1f">
    <Navbar />
    <FirstPage />
    <!-- <AboutUs /> -->
    <Benefits />
    <Advantages />
    <Programs />
    <v-main />
  </v-app>
</template>

<script lang="ts" setup>
import Navbar from "@/components/navigation_bar.vue";
import FirstPage from "./components/first_page.vue";
import AboutUs from "./components/about_us.vue";
import Benefits from "./components/benefits.vue";
import Advantages from "./components/advantages.vue";
import Programs from "./components/programs.vue";
</script>
