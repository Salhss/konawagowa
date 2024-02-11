<script>
import "../assets/colors.css";
import Hero from "../components/home/hero.vue";
export default {
  name: "home",
  components: { Hero },
};
</script>

<template>
  <div id="home">
    <Hero />
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
