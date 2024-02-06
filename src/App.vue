<template>
  <header>
    <img src="@/assets/konawa-logo.png" class="logo" />
    <div
      class="navbar-burger"
      @click="isOpen = !isOpen"
      :class="{ active: isOpen }"
    >
      <div class="line"></div>
      <div class="line"></div>
      <div class="line"></div>
    </div>
    <div class="menu-container">
      <div class="navbar-menu">
        <p>Beranda</p>
        <p>Event</p>
        <p>Partner Kami</p>
        <p>Keunggulan</p>
      </div>
    </div>
    
  </header>
  
  <RouterView />
  <div class="bottom-btn">
    <div class="btn-container">
      <p>Join Komunitas Kami</p>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import "./assets/colors.css";
import { RouterLink, RouterView } from "vue-router";

const isOpen = ref(false);
</script>

<style scoped>
p {
  font-family: "Inter", sans-serif;
}

@media (min-width: 360px) {
  header {
    padding-inline: 29px;
    padding-block: 12px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky;
    top: 0;
    background-color: var(--white);
  }
  .logo {
    width: 70px;
    height: auto;
  }
  .line {
    width: 35px;
    height: 5.7px;
    background-color: var(--red);
    border-radius: 5px;
  }
  .navbar-burger {
    display: flex;
    flex-direction: column;
    gap: 3px;
  }
  .navbar-burger .line {
    transition: all 300ms ease-in-out;
  }
  .navbar-burger.active .line:nth-child(1) {
    transform: rotate(-45deg) translate(-6px, 6px);
  }
  .navbar-burger.active .line:nth-child(2) {
    opacity: 0;
  }
  .navbar-burger.active .line:nth-child(3) {
    transform: rotate(45deg) translate(-6px, -6px);
  }
  .navbar-burger + .menu-container {
    transition: all 300ms ease-in-out;
  }
  .navbar-burger.active + .menu-container{
    right: 0;
  }
  .menu-container {
    position: absolute;
    top: 100%;
    width: 100%;
    background-color: rgba(217, 217, 217, 0.7);
    height: 100vh;
    right: 100%;
    z-index: 50;
  }
  .navbar-menu {
    background-color: var(--white);
    padding-inline: 48px;
    height: fit-content;
    display: flex;
    flex-direction: column;
    gap: 40px;
    padding-bottom: 100px;
  }
  .navbar-menu p {
    text-align: right;
    font-weight: 700;
    font-size: 25px;
    margin: 0;
  }
  .bottom-btn {
    position: sticky;
    position: -webkit-sticky;
    bottom: 0;
    height: 78px;
    background-color: var(--white-gray);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .btn-container {
    background-color: var(--red);
    color: var(--white-gray);
    font-weight: 700;
    padding-inline: 18px;
    border-radius: 5px;
    box-shadow: 0px 4px  4px rgba(0, 0, 0, 0.25);
  }
}
</style>
