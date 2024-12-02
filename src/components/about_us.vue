<template>
  <div class="about_us_container">
    <!-- Left side: Image -->
    <div class="left-side">
      <v-img
        src="/src/assets/people.svg"
        alt="People Image"
      />
    </div>
  
    <div class="right-side">
      <div class="centered-text">
        <div style="display: flex; flex-direction: column; border-left: 10px solid red; border-radius: 10px;">
          <span
            class="text-h2 ml-5"
            style="font-weight: bolder;"
          >About Us</span>  
          <span
            class="text-subtitle-2 mt-3 ml-5"
            style="font-weight: bold;"
          >Expert team</span>
        </div>

        <span class="mt-10">We are a team of professional fitness trainers with years 
          of experience and numerous successful collaborations. Health 
          is our top priority, and we believe that achieving your fitness 
          goals can significantly enhance self-esteem and confidence, positively 
          influencing all areas of your life. Therefore, training should be a lifestyle.</span>

        <br>

        <span>Our mission is to help people achieve their fitness goals.
          We have developed programs that have already delivered results, and 
          now you can order them here, tailored to your needs.</span>
      </div>
    </div>
  </div>
</template>
  

<style scoped>
.about_us_container {
  display: flex; 
  height: 100vh; 
  padding: 0 5rem;
  justify-content: center;
  align-items: center;
}

.left-side {
  flex: 1; 
  height: 80vh; 
  display: flex;
  justify-content: center;
  align-items: center;
}

.image {
  width: 100%;
  height: 100%; 
  object-fit: cover; 
}

.right-side {
  color: white !important;
  flex: 1; 
  display: flex;
  height: 80vh;
  flex-direction: column;
  justify-content: center; 
  text-align: start; 
  text-align: justify;
}

.centered-text {
  font-size: 24px; 
  color: white; 
  display: flex;
  flex-direction: column;
}
</style>
