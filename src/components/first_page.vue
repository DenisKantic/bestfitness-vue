<template>
  <div class="container" id="home">
    <div class="text-box">
      <span class="text-h2"
        >The possibilities are endless.Transform your life</span
      >
      <span class="heading"
        >Engaging in fitness provides numerous benefits for both body and mind,
        making it essential for overall health and well-being</span
      >
      <button class="button">Explore programs</button>
    </div>
  </div>
</template>

<style>
/* Base styles */
.container {
  height: 100vh;
  width: 100%;
  background-image: url("/src/assets/back_one.png");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}

.text-box {
  width: 80%;
  max-width: 600px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-end;
  overflow: hidden;
  background-color: rgba(31, 31, 31, 0.7);
  padding: 20px;
  box-sizing: border-box;
  border-radius: 2rem;
  color: white;
  text-align: left;
}

.text-box span {
  display: block;
  margin-bottom: 10px;
  font-weight: bolder;
}

.button {
  margin-top: 20px;
  display: inline-block;
  background-color: red;
  color: white;
  padding: 10px 20px;
  font-weight: lighter;
  margin: auto;
  border-radius: 2rem;
  font-size: 1rem;
  font-weight: bold;
  text-transform: uppercase;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

/* Hover state */
.button:hover {
  background-color: darkred;
}

/* Active state */
.button:active {
  background-color: darkred;
  transform: scale(0.98);
}

@media (max-width: 600px) {
  .text-box {
    width: 90%;
    top: 10%;
    padding: 15px;
    text-align: center;
    left: 0;
  }

  .text-h2 {
    font-size: 1.5rem !important;
    text-align: center;
    margin: auto;
  }

  .button {
    font-size: 0.9rem;
    padding: 8px 16px;
    margin: auto;
  }
}

/* Tablet */
@media (min-width: 601px) and (max-width: 768px) {
  .text-box {
    width: 80%;
    top: 15%;
    padding: 18px;
    margin-right: 2rem;
  }

  .text-h2 {
    font-size: 1.2rem !important;
  }

  .button {
    font-size: 1rem;
    padding: 9px 18px;
  }
}

/* Laptop / Small PC */
@media (min-width: 769px) and (max-width: 1024px) {
  .text-box {
    width: 70%;
    top: 20%;
    padding: 20px;
  }

  .text-h2 {
    font-size: 2rem;
  }

  .button {
    font-size: 1rem;
    padding: 10px 20px;
  }
}

/* PC / Large Devices */
@media (min-width: 1025px) {
  .text-box {
    width: 60%;
    max-width: 700px;
    position: relative;
    top: 15%;
    left: 20%;
    margin-right: 2rem;
    padding: 25px;
  }

  .text-h2 {
    font-size: 3rem !important;
  }

  .button {
    font-size: 1.2rem;
    padding: 12px 24px;
  }
}
</style>
.container { height: 100vh; width: 100%; background-image:
url("/src/assets/back_one.png"); background-size: cover; background-position:
center; background-repeat: no-repeat; display: flex; justify-content: center;
align-items: center; } .text-box { width: auto; display: flex; flex-direction:
column; justify-content: center; align-items: start; position: relative; top:
20%; right: 10%; transform: translateY(10%); background-color: rgba(255, 255,
255, 0.7); padding: 20px; box-sizing: border-box; border-radius: 2rem;
background-color: rgba(31, 31, 31, 0.7); } .text-box span { display: block;
margin-bottom: 10px; font-weight: bolder; } .button { margin: auto; display:
inline-block; background-color: red; color: white; padding: 10px 20px;
font-weight: lighter; border-radius: 2rem; font-size: 1rem; font-weight: bold;
text-transform: uppercase; border: none; cursor: pointer; margin-top: 20px;
z-index: 10 !important; transition: background-color 0.3s ease; /* Adding a
smooth transition for hover */ } /* Specific hover state */ .button:hover {
background-color: darkred; cursor: pointer; z-index: 20 !important; } /*
Specific active (click) state */ .button:active { background-color: darkred;
transform: scale(0.98); /* Optional: Add a slight scaling effect on click *
