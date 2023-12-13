<template>
    <div>
      <div class="gameintro">
        <div class="black-overlay"></div>
        <audio autoplay loop>
          <!-- <source src="../assets/creepy-audio.mp3" type="audio/mpeg"> -->
        </audio>
        <img src="../../assets/gameintro.jpg" alt="">
        <div class="centered-text">Murag Games</div>
        <button @click="startGame" class="creepy-button">Start Game</button>
      </div>
    </div>
  </template>
  <script>
    export default {
      methods: {
        startGame() {
          // Use Vue Router to navigate to the desired route
          this.$router.push('/intro'); // Replace '/intro' with your desired route
        },
      },
    };
    </script>
  
  <style>
  .gameintro {
    position: relative;
    height: 100vh;
  }
  
  .black-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: black;
    animation: fadeIn 3s ease-in;
    z-index: 2; /* Place the black overlay above the background image */
    opacity: 0; /* Initially transparent */
  }
  
  @keyframes fadeIn {
    from {
      opacity: 1;
    }
    to {
      opacity: 0;
    }
  }
  
  .gameintro img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    z-index: 1; /* Place the image below the black overlay */
  }
  
  .centered-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 100px;
    font-family: 'Your Halloween Font', cursive;
    color: #ff6600;
    text-shadow: 5px 5px 10px #000;
    z-index: 3; /* Place the text above the black overlay */
  }
  
  .creepy-button {
    position: fixed;
    bottom: 10px;
    left: 50%;
    transform: translateX(-50%);
    z-index: 4; /* Place the button above the black overlay */
    background-color: #731b1b;
    color: #fff;
    border: none;
    border-radius: 10px;
    padding: 15px 30px;
    cursor: pointer;
    font-size: 24px;
    text-transform: uppercase;
    font-weight: bold;
    letter-spacing: 2px;
    text-shadow: 2px 2px 5px #000;
    box-shadow: 0 0 20px #000;
    transition: background-color 0.3s, transform 0.3s;
    margin-bottom: 100px;
  }
  
  .creepy-button:hover {
    background-color: #4d0c0c;
    transform: translateX(-50%) scale(1.1);
  }
  </style>
  