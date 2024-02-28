<script>
import Hero from "@/components/home/Hero.vue";
import Benefit from "@/components/home/Benefit.vue";
import "../assets/colors.css";
import JoinCommunity from "@/components/home/JoinCommunity.vue";
import Events from "@/components/home/Events.vue";
import Galery from "@/components/home/Galery.vue";
export default {
  name: "home",
  components: { Hero, Benefit, JoinCommunity, Events, Galery },
};
</script>

<template>
  <div id="home">
    <Hero />
  </div>
  <div id="benefit">
    <Benefit />
  </div>
  <div id="join-community">
    <JoinCommunity />
  </div>
  <div id="events">
    <Events />
  </div>
  <div id="galery">
    <Galery />
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
