<template>
  <div
    id="advantages"
    class="d-flex flex-column ma-auto bg-container"
    style="
      min-height: 80vh;
      width: 100%;
      padding: 0 5rem;
      background: linear-gradient(to top left, red 50%, #1f1f1f 50%);
      overflow: hidden;
    "
  >
    <!-- Title Section -->
    <div
      class="h2-container"
      style="
        display: flex;
        flex-direction: column;
        border-left: 10px solid red;
        border-radius: 10px;
        margin-top: 5rem;
      "
    >
      <span class="text-h2 ml-5" style="font-weight: bolder; width: 50%"
        >Advantages of Choosing an Online Training and Nutrition Program</span
      >
    </div>

    <!-- Grid Layout Section -->
    <div
      style="
        margin-top: 2rem;
        text-align: justify;
        background-color: #1f1f1f;
        width: 100%;
      "
      class="grid-container"
    >
      <v-row :cols="12" :md="6" :lg="4" gutter="16" class="advantage-grid">
        <v-col v-for="n in 6" :key="n" cols="12" md="6" lg="4">
          <div>
            <div
              style="display: flex; align-items: center; margin-bottom: 2rem"
            >
              <span
                style="
                  display: flex;
                  justify-content: center;
                  align-items: center;
                  width: 2rem;
                  height: 2rem;
                  background-color: red;
                  color: black;
                  border-radius: 50%;
                  font-size: 1.5rem;
                  font-weight: bold;
                "
              >
                {{ n }}
              </span>
              <span style="font-size: 2rem; margin-left: 0.5rem">{{
                getTitle(n)
              }}</span>
            </div>

            <span style="font-size: 1.2rem">{{ getDescription(n) }}</span>
          </div>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  methods: {
    // Add type annotation for `n` as a number
    getTitle(n: number): string {
      const titles: string[] = [
        "Flexibility",
        "Access to Experts",
        "Supportive Community",
        "Variety of Content",
        "Cost-Effectiveness",
        "Progress Tracking",
      ];
      return titles[n - 1];
    },

    // Add type annotation for `n` as a number
    getDescription(n: number): string {
      const descriptions: string[] = [
        "Online programs allow you to train and eat according to your own schedule. You can tailor workouts and meals to fit your daily commitments, making it easier to incorporate healthy habits into your life.",
        "With online programs, you have the opportunity to consult with qualified trainers and nutritionists from the comfort of your home. This enables personalized advice and support without the need for physical presence.",
        "Many online programs provide access to communities or forums where you can share experiences, ask questions, and receive support from others facing similar challenges.",
        "Many online programs offer a wide range of exercises and recipes, which can help maintain motivation and diversity in your training and nutrition.",
        "Online programs are often more affordable than traditional gyms or personal trainers, reducing costs without sacrificing quality.",
        "Using digital tools makes it easier to track your progress, whether it's weight loss, strength gains, or improved endurance. This can further motivate you and help you stay on track.",
      ];
      return descriptions[n - 1];
    },
  },
};
</script>

<style scoped>
/* Mobile */
@media (max-width: 600px) {
  /* Remove red background on mobile */
  .d-flex {
    background: none;
  }

  .grid-container {
    padding: 0 !important;
  }
  .bg-container {
    width: 100%;
    padding: 0 !important;
    background: none !important ;
  }

  /* Set grid width to 90% on mobile */
  .advantage-grid {
    width: 100%;
    padding: 0;
    margin: 0 auto;
    gap: 1rem;
  }

  .h2-container {
    border-left: none !important;
  }

  .text-h2 {
    font-size: 1.8rem !important;
    width: 90% !important;
  }

  .v-row {
    padding: 0 1rem;
  }

  .v-col {
    padding: 0.5rem;
  }

  .text-h4 {
    font-size: 1rem;
  }

  .text-body-1 {
    font-size: 0.9rem;
  }

  .v-col .v-btn {
    font-size: 0.9rem;
  }
}

/* Tablets (Medium devices) */
@media (min-width: 601px) and (max-width: 1024px) {
  .text-h2 {
    font-size: 1.5rem;
    width: 80% !important;
  }

  .v-row {
    padding: 0 2rem;
  }

  .v-col {
    padding: 1rem;
  }

  .text-h4 {
    font-size: 1.25rem;
  }

  .text-body-1 {
    font-size: 1.1rem;
  }

  .v-col .v-btn {
    font-size: 1.1rem;
  }

  .grid-container {
    padding-bottom: 2rem;
    margin-bottom: 2rem;
  }
}

/* Large devices (desktops) */
@media (min-width: 1025px) {
  .text-h2 {
    font-size: 2.5rem;
  }

  .grid-container {
    padding: 2rem 0rem;
    margin-bottom: 2rem;
    height: auto;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  /*
    .advantage-grid{
        gap: 2rem;
    } */

  .v-row {
    padding: 0 2rem;
  }

  .v-col {
    padding: 2rem;
  }

  .text-h4 {
    font-size: 1.5rem;
  }

  .text-body-1 {
    font-size: 1.2rem;
  }

  .v-col .v-btn {
    font-size: 1.2rem;
  }
}
</style>
