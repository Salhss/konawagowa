<script>
import Hero from "@/components/home/Hero.vue";
import Benefit from "@/components/home/Benefit.vue";
import "../assets/colors.css";
export default {
  name: "home",
  components: { Hero, Benefit },
};
</script>

<template>
  <div id="home">
    <Hero />
  </div>
  <div id="benefit">
    <Benefit />
  </div>
</template>

<style scoped>
#home {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 26px;
  padding-inline: 15px;
  background-color: var(--red-default);
}
</style>
