<template>
  <div
    class="nav-container"
    style="height: 2vh; position: fixed; top: 0; left: 0; right: 0"
  >
    <v-navigation-drawer v-model="drawer" disable-resize-watcher>
      <v-list nav>
        <v-list-item v-for="(item, i) in items" :key="i" :active="i === 0" link>
          <v-list-item-title>{{ item.text }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar fixed flat class="px-16" color="red">
      <template #prepend>
        <v-app-bar-nav-icon
          v-if="$vuetify.display.smAndDown"
          @click="drawer = !drawer"
        />
      </template>

      <v-img class="me-sm-8" max-width="80" src="/src/assets/logo_best.svg" />

      <template v-if="$vuetify.display.mdAndUp">
        <v-btn
          v-for="(item, i) in items"
          :key="i"
          :active="i === 0"
          class="me-2 text-none"
          style="font-size: 1.2rem"
        >
          {{ item.text }}
        </v-btn>
      </template>

      <v-spacer />

      <template #append>
        <v-btn
          class="ms-1"
          btn
          style="
            background-color: white;
            color: black;
            border-radius: 2rem;
            font-size: 0.8rem;
          "
        >
          Contact Us
        </v-btn>
      </template>
    </v-app-bar>
  </div>
</template>

<script lang="ts">
import { ref } from "vue";

export default {
  setup() {
    const drawer = ref(false);

    const items = [
      { text: "Home" },
      { text: "About" },
      { text: "Benefits" },
      { text: "Programs" },
    ];

    return { drawer, items };
  },
};
</script>

<style scoped>
.v-navigation-drawer {
  z-index: 2000; /* Higher z-index for the navigation drawer */
}

.v-app-bar {
  z-index: 2100; /* Ensure the app bar stays on top of everything */
}

.nav-container {
  z-index: 1000;
}
</style>
