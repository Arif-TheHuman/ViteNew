<template>
  <div class="container">
    <div class="profile">
      <img class="logo"src="./assets/images/profile.jpeg" alt="Profile Picture" />
      <div class="menacing" id="menacing1">
        <img src="./assets/images/menacing.png" alt="Menacing..." class="menacess">
      </div>
      <div class="menacing" id="menacing2">
        <img src="./assets/images/menacing.png" alt="Menacing..." class="menacess">
      </div>
      <div class="menacing" id="menacing3">
        <img src="./assets/images/menacing.png" alt="Menacing..." class="menacess">
      </div>
      <div class="menacing" id="menacing4">
        <img src="./assets/images/menacing.png" alt="Menacing..." class="menacess">
      </div>
    </div>
  </div>
</template>

<style scoped>

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

.menacess {
  width: 50px;
  height: 50px;
  position: absolute;
  opacity: 0;
  transition: opacity 600ms;
}

.container:hover .menacess {
  opacity: 1;
  animation: shake 0.5s; /* Apply the shake animation */
  animation-iteration-count: infinite;
}

#menacing1 .menacess {
  top: -10px;
  left: -10px;
}

#menacing2 .menacess {
  top: -10px;
  right: -10px;
}

#menacing3 .menacess {
  bottom: -10px;
  left: -10px;
}

#menacing4 .menacess {
  bottom: -10px;
  right: -10px;
}

.logo {
  border-radius: 50%;
  height: 20vw;
  max-height: 200px;
  min-height: 100px;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
  object-fit: cover;
}

.profile {
  position: relative;
  border-radius: 50%;
  height: 20vw;
  max-height: 200px;
  min-height: 100px;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
  object-fit: cover;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #5900b3aa);
}
</style>