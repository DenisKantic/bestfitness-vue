<template>
  <div
    style="min-height: 100vh; width: 100%; padding: 0 5rem"
    class="d-flex flex-column items-center justify-center container"
  >
    <h1 style="font-size: 2rem; text-align: center">Programs</h1>

    <span style="text-align: center; width: 50%">
      Choosing our online training and nutrition program offers flexibility,
      expertise, and support, making it easier to achieve your fitness goals in
      an effective and sustainable way. Please select the program that best
      meets your needs. Begin by choosing between a Personal or Universal
      program, followed by selecting the desired intensity level.
    </span>

    <!-- Cards Grid -->
    <div
      style="
        display: grid;
        grid-template-columns: repeat(2, 1fr); /* Two equal-width columns */
        gap: 2rem; /* Adds space between the cards */
      "
    >
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
  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {
      activeGroup: 1,
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
      ],
    };
  },
  methods: {
    toggleGroup(groupNumber) {
      this.activeGroup = groupNumber;
    },
  },
};
</script>

<style scoped>
.container {
  height: 100vh;
  width: 100%;
  background-image: url("/src/assets/programs_bg.svg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  overflow: hidden;
}

/* Card Styles */
.card {
  margin: 10px;
  padding: 20px;
  background-color: #f0f0f0;
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
}

.card-description {
  font-size: 1rem;
  color: #333;
}

/* Media Query for Mobile Devices */
@media (max-width: 768px) {
  /* Adjust the grid layout to a single column on small screens */
  .container {
    padding: 0 2rem; /* Adjust padding for smaller screens */
  }
  .card-grid {
    grid-template-columns: repeat(
      3,
      1fr
    ) !important; /* Single column layout for mobile */
  }

  .card {
    padding: 15px; /* Reduce padding inside the cards on smaller screens */
    margin: 5px; /* Adjust margin */
  }

  /* Stack cards vertically on mobile */
  .d-flex {
    display: block;
  }

  div[style*="display: grid"] {
    grid-template-columns: 1fr; /* Stack cards in a single column */
  }
}
</style>
