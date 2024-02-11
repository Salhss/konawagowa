<script>
import '@/assets/colors.css'
export default {
    name: "hero-section",
    mounted() {
      document.addEventListener("DOMContentLoaded", function (event) {
  // array with texts to type in typewriter
  var dataText = [
    "Smart",
    "Solid",
    "Happy"
  ];

  // type one text in the typwriter
  // keeps calling itself until the text is finished
  function typeWriter(text, i, fnCallback) {
    // chekc if text isn't finished yet
    if (i < text.length) {
      // add next character to h1
      document.getElementById("typed-content").innerHTML =
        text.substring(0, i + 1) + '<span aria-hidden="true"></span>';

      // wait for a while and call this function again for next character
      setTimeout(function () {
        typeWriter(text, i + 1, fnCallback);
      }, 100);
    }
    // text finished, call callback if there is a callback function
    else if (typeof fnCallback == "function") {
      // call callback after timeout
      setTimeout(fnCallback, 700);
    }
  }
  // start a typewriter animation for a text in the dataText array
  function StartTextAnimation(i) {
    if (typeof dataText[i] == "undefined") {
      setTimeout(function () {
        StartTextAnimation(0);
      }, 1000);
    }
    // check if dataText[i] exists
    if (i < dataText[i]?.length) {
      // text exists! start typewriter animation
      typeWriter(dataText[i], 0, function () {
        // after callback (and whole text has been animated), start next text
        StartTextAnimation(i + 1);
      });
    }
  }
  // start the text animation
  StartTextAnimation(0);
});
    }
}
</script>

<template>
  <div class="hero-container">
    <div class="hero-banner">
      <img src="@/assets/images/hero-banner.jpeg" class="hero-image"/>
    </div>
    <div class="hero-content">
      <div class="hero-text">
        <p>Sehat Bersama Kami</p>
        <div class="type-text">
          <p class="untype">Komunitas Ter -</p>
          <div class="typed-container">
            <p id="typed-content" class="typed">Happy</p>
          </div>
        </div>
        <p>No. 1 di <span class="gowa">gowa !</span></p>
        <p class="small-text">Cek Agenda Sehat Kami Sekarang</p>
      </div>
      <div class="action-btn">
        <div class="agenda-btn">
          <p>Lihat Agenda</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .hero-banner {
    width: 90%;
    height: 400px;
  }
  .hero-image {
    object-fit: cover;
    object-position: center;
    border-radius: 20px;
    width: 100%;
    height: 100%;
  }
  .hero-text p {
    text-align: left;
    font-weight: 700;
    color: var(--white-bone);
  }
  .typed-container {
    background-color: var(--white-bone);
    width: 150px;
    height: 45px;
    border-radius: 5px;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    border: 1px rgba(0, 0, 0, 0.25);
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .type-text {
    display: flex;
    align-items: center;
  }
  .typed {
    color: var(--red-default) !important;
    margin: 0;
  }
  .gowa {
    text-transform: uppercase;
    letter-spacing: 2px;
    font-size: larger;
  }
  .small-text {
    font-weight: 500 !important;
  }
  
  .agenda-btn {
    border: solid 1px rgba(0, 0, 0, 0.25);
    background-color: var(--red);
    width: fit-content;
    height: fit-content;
    box-shadow: 0 4px 4px rgba(0, 0, 0, 0.25);
  }
  .agenda-btn p {
    margin: 0;
    font-weight: 700;
    color: white;
  }

@media (min-width: 1021px) {
  .hero-container {
    gap: 28px;
    justify-content: space-between;
  }
  .hero-banner {
    width: 580px;
    height: 380px;
    margin-bottom: 40px;
  }
  .hero-content {
    margin-top: 20px;
  }
  .hero-content p {
    font-size: 28px;
    margin-block: 10px;
  }
  .typed-container {
    margin-left: 12px;
    height: 50px;
  }
  .small-text {
    font-size: 20px !important;
    margin-top: 20px !important;
  }
  .action-btn {
    margin-top: 40px;
  }
  .agenda-btn {
    padding-inline: 40px;
    border-radius: 8px;
    cursor: pointer;
    transition: all 200ms ease-in-out;
  }
  .agenda-btn p {
    font-size: 24px;
  }
  .agenda-btn:hover {
    box-shadow: none;
    transform: translateY(4px);
  }
}

@media (min-width: 761px) and (max-width: 1020px) {
  .hero-container {
    gap: 24px;
  }
  .hero-banner {
    width: 60%;
    height: 300px;
    margin-bottom: 30px;
  }
  .hero-content {
    width: 45%;
  }
  .hero-text {
    margin-top: 10px;
  }
  .hero-text p {
    font-size: 20px;
    margin-block: 10px;
  }
  .small-text {
    font-size: 16px !important;
  }
  .typed-container {
    margin-left: 8px;
    width: 135px;
  }
  .action-btn {
    margin-top: 44px;
  }
  .agenda-btn {
    padding-block: 12px;
    padding-inline: 28px;
    border-radius: 8px;
  }
  .agenda-btn p {
    font-size: 20px;
  }
 
}

@media (min-width: 761px) {
  .hero-container {
    display: flex;
    flex-direction: row-reverse;
  }
}

@media (max-width: 760px) {
  .hero-banner {
    width: 90%;
    height: 400px;
  }
  .hero-image {
    object-fit: cover;
    object-position: center;
    border-radius: 20px;
    width: 100%;
    height: 100%;
  }
  .hero-text {
    width: 100%;
  }
  .hero-text p {
    font-size: 24px;
    margin-block: 8px;
  }
  .typed-container {
    margin-left: 10px;
  }
}

@media (max-width: 430px) {
  .hero-banner {
    width: 100%;
    height: 242px;
  }
  .small-text {
    font-size: 16px !important;
  }
  .action-btn {
    display: flex;
    justify-content: center;
    margin-top: 40px;
    margin-bottom: 60px;
  }
  .agenda-btn {
    padding-block: 12px;
    padding-inline: 24px;
    border-radius: 5px;
  }
  .agenda-btn p {
    font-size: 24px;
  }
  .typed-container {
    width: 130px;
  }
}
</style>