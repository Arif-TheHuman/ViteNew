<script setup lang="ts">

</script>

<template>
  <div>
      <img src="./assets/images/profile.jpeg" class="logo vue" alt="Profile Picture" />
  </div>
</template>

<style scoped>
.logo {
  border-radius: 50%; /* Make the image circular */
  height: 20vw; /* Set the height relative to the viewport width */
  max-height: 200px; /* Set a maximum height */
  min-height: 100px; /* Set a minimum height */
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
  object-fit: cover; /* Ensure the image covers the entire area of the div */
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
