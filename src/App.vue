<template>
  <div id="firstDiv" class="relative flex flex-col md:flex-row border-4 border-purple-600 p-5 backdrop-blur">
    <br>
    <div class="relative flex justify-start md:justify-center lg:justify-start items-center mb-4 md:mb-0">
      <div class="relative w-64 h-64 mx-auto md:w-72 md:h-72 lg:w-80 lg:h-80">
        <img class="w-full h-full object-cover rounded-full hover:shadow-purple-glow transition-shadow duration-500 ease-in-out" src="./assets/images/profile.jpg" alt="Profile Picture" 
             @mouseover="isHovered = true" 
             @mouseleave="isHovered = false" />
        <div class="absolute top-0 left-0 w-12 h-12 transition-opacity duration-100 linear" 
             :class="{'opacity-0': !isHovered, 'opacity-100': isHovered, 'animate-shake': isHovered}" id="menacing1">
          <img src="./assets/images/menacing.png" alt="Menacing..." class="w-full h-full object-cover transition duration-200 ease-in-out">
        </div>
        <div class="absolute top-0 right-0 w-12 h-12 transition-opacity duration-600 ease-in-out" 
             :class="{'opacity-0': !isHovered, 'opacity-100': isHovered, 'animate-shake': isHovered}" id="menacing2">
          <img src="./assets/images/menacing.png" alt="Menacing..." class="w-full h-full object-cover transition duration-200 ease-in-out">
        </div>
        <div class="absolute bottom-0 left-0 w-12 h-12 transition-opacity duration-600 ease-in-out" 
             :class="{'opacity-0': !isHovered, 'opacity-100': isHovered, 'animate-shake': isHovered}" id="menacing3">
          <img src="./assets/images/menacing.png" alt="Menacing..." class="w-full h-full object-cover transition duration-200 ease-in-out">
        </div>
        <div class="absolute bottom-0 right-0 w-12 h-12 transition-opacity duration-600 ease-in-out" 
             :class="{'opacity-0': !isHovered, 'opacity-100': isHovered, 'animate-shake': isHovered}" id="menacing4">
          <img src="./assets/images/menacing.png" alt="Menacing..." class="w-full h-full object-cover transition duration-200 ease-in-out">
        </div>
      </div>
    </div>
    <span class="pl-10 md:pl-20">
      <h1 class="text-2xl md:text-3xl lg:text-4xl font-bold text-purple-400">Arif-TheHuman</h1>
      <p class="pt-3">Hello! My real name is Muhammad Nur Arif Bin Abdullah Hidup.</p>
      <p class="pt-3">Certified Cat Lover</p>
      <p class="pt-3">Professional Human, 10+ Years of Experience</p>
      <p class="pt-3">Favourite Show: Jojo's Bizzare Adventure</p>
      <p class="pt-3">Hover On My Profile To See Something Cool!</p>
      <p class="pt-3">Hello world</p>
    </span>
  </div>
  <div v-if="showKillerQueen" class="fixed bottom-0 right-0 transform translate-x-1/2 translate-y-1/2">
    <img class="w-full max-w-xs sm:max-w-xs md:max-w-sm lg:max-w-md xl:max-w-lg" src="./assets/images/killerqueen.webp" alt="Killer_Queen"> 
  </div>
</template>

<script>
export default {
  data() {
    return {
      isHovered: false,
      showKillerQueen: false,
    };
  },
  methods: {
  playAudio() {
    const audio = new Audio('./src/assets/audio/killerQueen.mp3');
    const audio1 = new Audio('./src/assets/audio/killerqueenSFX_Updated.mp3');
    audio.play();
    this.showKillerQueen = !this.showKillerQueen;
    audio.onended = () => {
      audio1.play();
      document.body.style.backgroundImage = "url('./src/assets/images/bg-reverse.gif')";
    };
    audio1.onended = () => {
      document.body.style.backgroundImage = "url('./src/assets/images/bg.gif')";
      this.showKillerQueen = !this.showKillerQueen;
    };
  },
},
};
</script>

<style scoped>

#firstDiv.backdrop-blur {
  backdrop-filter: blur(10px);
}

@keyframes shake {
  0% { transform: translate(1px, 1px) rotate(0deg); }
  10% { transform: translate(-1px, -2px) rotate(-1deg); }
  20% { transform: translate(-3px, 0px) rotate(1deg); }
  30% { transform: translate(3px, 2px) rotate(0deg); }
  40% { transform: translate(1px, -1px) rotate(1deg); }
  50% { transform: translate(-1px, 2px) rotate(-1deg); }
  60% { transform: translate(-3px, 1px) rotate(0deg); }
  70% { transform: translate(3px, 1px) rotate(-1deg); }
  80% { transform: translate(-1px, -1px) rotate(1deg); }
  90% { transform: translate(1px, 2px) rotate(0deg); }
  100% { transform: translate(1px, -2px) rotate(-1deg); }
}
.animate-shake {
  animation: shake 0.5s; /* Apply the shake animation */
  animation-iteration-count: infinite;
}
.hover\:shadow-purple-glow:hover {
  box-shadow: 0 0 10px #4e0ed0, 0 0 20px #4e0ed0, 0 0 30px #4e0ed0, 0 0 40px #4e0ed0;
}
body {
  overflow: hidden;
}
</style>