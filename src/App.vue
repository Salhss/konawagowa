<template>
  <header>
    <img src="@/assets/konawa-logo.png" class="logo" />
    <nav class="navbar-container">
      <ul>
        <li>Beranda</li>
        <li>Event</li>
        <li>Partner Kami</li>
        <li>Keunggulan</li>
      </ul>
    </nav>
    <div class="user-btn">
      <div class="join-btn">
        <JoinButton />
      </div>
      <NavbarMobile :isOpen="isOpen" />
    </div>
  </header>

  <RouterView />

  <div class="bottom-btn">
    <JoinButton />
  </div>
</template>

<script setup>
import { ref } from "vue";
import "./assets/colors.css";
import { RouterLink, RouterView } from "vue-router";
import NavbarMobile from "./components/layout/NavbarMobile.vue";
import JoinButton from "./components/ui/JoinButton.vue";

const isOpen = ref(false);
</script>

<style scoped>
.bottom-btn {
  display: none;
}

.navbar-container {
  display: none;
}

@media (min-width: 1301px) {
  .navbar-container ul {
    gap: 22px;
    font-size: 24px;
  }
}

@media (max-width: 1300px) {
  .navbar-container ul {
    gap: 22px;
  }
  .logo {
    width: 70px;
  }
}

@media (min-width: 913px) {
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-block: 15px;
    padding-left: 30px;
    position: sticky;
    top: 0;
    background-color: var(--white);
  }
  .navbar-container{
    display: block;
  }
  .navbar-container ul {
    display: flex;
    list-style-type: none;
    font-weight: 700;
  }
  .navbar-container li {
    cursor: pointer;
  }
  .navbar-container li:hover {
    color: var(--red);
  }
  .join-btn {
    display: flex;
    align-items: end;
    justify-content: flex-end;
    transition: all 200ms ease-in-out;
  }
  .join-btn:hover {
    transform: translateY(5px);
  }
}

@media (max-width: 912px) {
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
    height: auto;
    width: 60px;
  }
  .user-btn {
    height: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .join-btn {
    display: flex;
    align-items: center;
    height: 50px;
    margin-right: 20px;
  }
  
}

@media (max-width: 500px) {
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
  .join-btn {
    display: none;
  }
}
</style>
