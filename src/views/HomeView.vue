<script setup>
import '../assets/colors.css'
</script>

<template>
  <main>
    <div class="hero-banner">
      <img src="@/assets/images/hero-banner.jpeg" class="hero-image"/>
    </div>
    
  </main>
</template>

<style scoped>
main {
  height: 100vh;
  background-color: var(--red-default);
}



@media (max-width: 912px) {
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: 26px;
    padding-inline: 15px;
  }
  .hero-banner {
    width: 100%;
    height: 242px;
  }
  .hero-image {
    object-fit: cover;
    object-position: center;
    border-radius: 20px;
    width: 100%;
    height: 100%;
  }
  
}
</style>