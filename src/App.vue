<template>
  <v-app style="margin: 0; background-color: #1f1f1f">
    <Navbar />
    <FirstPage />
    <AboutUs />
    <Benefits />
    <Advantages />
    <Programs />

    <v-footer color="red" height="5vh">
      <span class="text-white" style="text-align: center; width: 100%">
        Best Fitness 2024 <v-icon small class="ml-2">mdi-copyright</v-icon>
      </span>
    </v-footer>
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
