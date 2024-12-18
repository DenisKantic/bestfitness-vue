<template>
  <div
    id="programs"
    style="height: 100vh; width: 100%; padding: 0 5rem"
    class="d-flex flex-column items-center justify-center container"
  >
    <h1 style="font-size: 2rem; text-align: center" class="title">Programs</h1>

    <span class="text-box-container">
      Choosing our online training and nutrition program offers flexibility,
      expertise, and support, making it easier to achieve your fitness goals in
      an effective and sustainable way. Please select the program that best
      meets your needs. Begin by choosing between a Personal or Universal
      program, followed by selecting the desired intensity level.
    </span>

    <!-- Cards Grid -->
    <div class="card-grid">
      <div
        v-for="(card, index) in activeGroup === 1 ? group1 : group2"
        :key="index"
        class="card"
      >
        <h3 class="card-title">{{ card.title }}</h3>
        <div class="card-description">
          <p v-html="card.description"></p>
        </div>
      </div>
    </div>

    <div class="trainer-container">
      <span>Choose your trainer</span>
      <div class="persons">
        <v-btn
          color="primary"
          href="mailto:leonardolukic9@gmail.com"
          style="z-index: 2"
        >
          <v-icon class="mr-2">mdi-email</v-icon>
          Leonardo
        </v-btn>

        <v-btn color="secondary"
          ><v-icon
            href="mailto:abest2802@gmail.com"
            style="margin-right: 0.5rem; z-index: 2"
            >mdi-email</v-icon
          >
          Andrea</v-btn
        >
      </div>
    </div>
  </div>
</template>

<script lang="ts">
interface Card {
  title: string;
  description: string;
}

export default {
  data() {
    return {
      activeGroup: 1 as number,
      group1: [
        {
          title: "Personal",
          description: `
                  Only nutrition program (€39.99) <br>
                  Only nutrition program with full meal recipes (€49.99) <br>
                  Home training program (€44.99) <br>
                  Home nutrition and training program (€69.99) <br>
                  Home nutrition and training program with full meal recipes (€79.99) <br>
                  Gym training program (€34.99) <br>
                  Gym nutrition and training program (€44.99) <br>
                  Gym nutrition and training program with full meal recipes (€69.99)
                `,
        },
        {
          title: "Universal",
          description: `
    Only nutrition program (€19.99) <br>
    Only nutrition program with full meal recipes (€29.99) <br>
    Home training program (€24.99) <br>
    Home nutrition and training program (€39.99) <br>
    Home nutrition and training program with full meal recipes (€49.99) <br>
    Gym training program (€24.99) <br>
    Gym nutrition and training program (€34.99) <br>
    Gym nutrition and training program with full meal recipes (€44.99)
  `,
        },
      ] as Card[], // Ensure group1 is typed as an array of `Card`
      group2: [
        {
          title: "Personal",
          description: `
                  Only nutrition program (€39.99) <br>
                  Only nutrition program with full meal recipes (€49.99) <br>
                  Home training program (€44.99) <br>
                  Home nutrition and training program (€69.99) <br>
                  Home nutrition and training program with full meal recipes (€79.99) <br>
                  Gym training program (€34.99) <br>
                  Gym nutrition and training program (€44.99) <br>
                  Gym nutrition and training program with full meal recipes (€69.99)
                `,
        },
        {
          title: "Universal",
          description: `
    Only nutrition program (€19.99) <br>
    Only nutrition program with full meal recipes (€29.99) <br>
    Home training program (€24.99) <br>
    Home nutrition and training program (€39.99) <br>
    Home nutrition and training program with full meal recipes (€49.99) <br>
    Gym training program (€24.99) <br>
    Gym nutrition and training program (€34.99) <br>
    Gym nutrition and training program with full meal recipes (€44.99)
  `,
        },
      ] as Card[], // Ensure group2 is typed as an array of `Card`
    };
  },
  methods: {
    toggleGroup(groupNumber: number) {
      this.activeGroup = groupNumber;
    },
  },
};
</script>

<style scoped>
.container {
  min-height: 100vh !important;
  width: 100%;
  background-image: url("/src/assets/programs_bg.svg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center !important;
}

.title {
  padding-bottom: 3rem;
  font-size: 4rem !important;
}
/* Card Styles */
.card {
  margin: 10px;
  padding: 20px;
  background-color: #fff;
  border-radius: 8px;
  text-align: left;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
  cursor: pointer;
  min-height: 250px;
}

.card-title {
  font-size: 1.25rem;
  font-weight: bold;
  color: red;
  margin-bottom: 10px;
  text-align: center;
  font-weight: bold;
}

.card-description {
  font-size: 1rem;
  color: #333;
}

/* Default Grid Layout (for larger screens) */
.card-grid {
  padding-top: 2rem;
  display: grid;
  grid-template-columns: repeat(2, 1fr); /* Two columns for larger screens */
  gap: 20px;
  width: auto;
}

.trainer-container {
  padding-top: 2rem;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  font-size: 1.2rem;
}

.persons {
  padding-top: 1.5rem;
  display: flex;
  flex-direction: row;
  gap: 2rem;
}

/* Media Query for Mobile Devices */
@media (max-width: 768px) {
  .container {
    padding: 2rem !important; /* Adjust padding for smaller screens */
    width: 100% !important;
    height: auto !important;
  }

  .text-box {
    width: 100%;
  }

  .card-grid {
    grid-template-columns: 1fr; /* Single column layout for mobile */
    grid-template-rows: auto; /* Adjust rows for mobile */
  }

  .text-box-container {
    text-align: justify;
  }

  .card {
    padding: 15px; /* Reduce padding inside the cards on smaller screens */
    margin: 5px; /* Adjust margin */
  }
}

@media (min-width: 1000px) {
  .text-box-container {
    width: 60%;
    text-align: center;
    font-size: 1.5rem;
  }
}
</style>
