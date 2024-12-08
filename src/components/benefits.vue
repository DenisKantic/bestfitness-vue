<template>
  <div
    style="height: 100vh; width: 100%; padding: 0 5rem; overflow: hidden"
    class="d-flex flex-column ma-auto"
  >
    <div style="display: flex; flex-direction: column; border-left: 10px solid red; border-radius: 10px;">
      <span
        class="text-h2 ml-5"
        style="font-weight: bolder;"
      >The Benefits of Fitness</span>  
      <span
        class="text-subtitle-2 mt-3 ml-5"
        style="font-weight: bold;"
      >Here are some fundamental aspects of fitness and reasons why we should engage in it</span>
    </div>

    <!-- grid layout -->
    <div
      style="display: grid; grid-template-columns: 1fr 1fr; grid-template-rows: 1fr 1fr 1fr; gap: 5rem; margin-top: 6rem;"
    >
      <div
        class="d-flex align-center"
        style="width: 80%;"
      >
        <v-img
          src="/src/assets/Group.svg"
          class="d-flex"
          height="100%"
          width="auto"
        />
  
        <!-- Text content to the right of the image -->
        <div class="ml-4">
          <span class="text-h4">Physical Health</span> <br>
          <span class="subtext-1">Regular physical activity improves cardiovascular health, strengthens muscles and bones, 
            and reduces the risk of various diseases such as diabetes and hypertension</span>
        </div>
      </div>

      <div
        class="d-flex align-center"
        style="width: 80%;"
      >
        <v-img
          src="/src/assets/iconoir_brain.svg"
          class="d-flex"
          height="100%"
          width="auto"
        />
        <div class="ml-4">
          <span class="text-h4">Mental Health</span> <br>
          <span class="subtext-1">Exercise can reduce symptoms of anxiety and depression, improve mood, and 
            increase energy levels thanks to the release of endorphins</span>
        </div>
      </div>
      <div
        class="d-flex align-center"
        style="width: 80%;"
      >
        <v-img
          src="/src/assets/hugeicons_weight-scale.svg"
          class="d-flex"
          height="100%"
          width="auto"
        />
        <div class="ml-4">
          <span class="text-h4">Weight Management</span> <br>
          <span class="subtext-1">Fitness helps maintain a healthy body weight and is one of the key factors in weight lossFitness helps maintain a
            healthy body weight and is one of the key factors in weight loss</span>
        </div>
      </div>
      <div
        class="d-flex align-center"
        style="width: 80%;"
      >
        <v-img
          src="/src/assets/icon_eqipment.svg"
          class="d-flex"
          height="100%"
          width="auto"
        />

        <div class="ml-4">
          <span class="text-h4">Increased Endurance and Strength</span> <br>
          <span class="subtext-1">Regular exercise improves physical endurance, making daily activities easier, and increases muscle strength</span>
        </div>
      </div>
      <div
        class="d-flex align-center"
        style="width: 80%;"
      >
        <v-img
          src="/src/assets/icon_fitness_zones.svg"
          class="d-flex"
          height="100%"
          width="auto"
        />

        <div class="ml-4">
          <span class="text-h4">Flexibility </span> <br>
          <span class="subtext-1">Stretching and mobility exercises improve flexibility, which can help prevent injuries</span>
        </div>
      </div>
      <div
        class="d-flex align-center"
        style="width: 80%;"
      >
        <v-img
          src="/src/assets/social.svg"
          class="d-flex"
          height="100%"
          width="auto"
        />

        <div class="ml-4">
          <span class="text-h4">Social Aspect </span> <br>
          <span class="subtext-1">Fitness can also be a social activity, whether through group workouts, sports, or 
            shared activities, which encourages connecting with others</span>
        </div>
      </div>
    </div>
  </div>
</template>