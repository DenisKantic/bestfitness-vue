<template>
  <div class="container">
    <div class="text-box">
      <span class="text-h2">The possibilities are endless. <br>Transform your life</span>
      <span>Engaging in fitness provides numerous benefits for both body 
        and <br> mind, making it essential for  overall health and well-being</span>
      <button class="button"> 
        Explore programs
      </button>
    </div>
  </div>
</template>

<style>
.container {
  height: 100vh;
  width: 100%;
  background-image: url('/src/assets/back_one.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  justify-content: flex-end; 
  align-items: center; 
  padding-right: 10%; 
}

.text-box {
  width: auto; 
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: start;
  position: absolute;
  top: 20%; 
  right: 10%;
  transform: translateY(10%); 
  background-color: rgba(255, 255, 255, 0.7); 
  padding: 20px;
  box-sizing: border-box; 
  border-radius: 2rem;
  background-color: rgba(31, 31, 31, 0.7);
}

.text-box span {
  display: block;
  margin-bottom: 10px;
  font-weight: bolder;
}


.button {
  margin: auto;
  display: inline-block;
  background-color: red;
  color: white;
  padding: 10px 20px;
  font-weight: lighter;
  border-radius: 2rem;
  font-size: 1rem;
  font-weight: bold;
  text-transform: uppercase;
  border: none;
  cursor: pointer;
  margin-top: 20px;
  z-index: 10 !important;
  transition: background-color 0.3s ease; /* Adding a smooth transition for hover */
}

/* Specific hover state */
.button:hover{
  background-color: darkred;
  cursor: pointer;
  z-index: 20 !important;
}

/* Specific active (click) state */
.button:active {
  background-color: darkred;
  transform: scale(0.98); /* Optional: Add a slight scaling effect on click */
}

</style>
