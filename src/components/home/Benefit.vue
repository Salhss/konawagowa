<script>
import "@/assets/colors.css";
export default {
  name: "benefit",
};
</script>
<template>
  <h1 class="benefit-head">Beragam Keseruan<br />Yang Bisa Kamu Dapatkan</h1>
  <div class="image-background">
    <div class="image-container">
      <img
        src="@/assets/images/benefit-image.jpeg"
        alt="poundfit konawa"
        class="benefit-img"
      />
    </div>
  </div>
  <div class="benefits-container">
    <div class="benefits-left">
      <div class="benefit-item">
        <div class="logo-container">
          <img
            src="../../assets/images/poundfit-black.png"
            alt="konawa poundfit"
            class="benefit-logo poundfit"
          />
        </div>
        <p>Senam Poundfit</p>
      </div>
      <div class="benefit-item">
        <div class="logo-container">
          <img
            src="../../assets/images/zumba-logo.png"
            alt="konawa zumba"
            class="zumba"
          />
        </div>
        <p>Senam Zumba</p>
      </div>
      <div class="benefit-item">
        <div class="logo-container">
          <img
            src="../../assets/svgs/community.svg"
            alt="komunitas seru"
            loading="lazy"
            class="community"
          />
        </div>
        <p>Komunitas Seru</p>
      </div>
    </div>
    <div class="middle-image-background">
      <div class="image-container">
        <img
          src="@/assets/images/benefit-image.jpeg"
          alt="poundfit konawa"
          class="benefit-img"
        />
      </div>
    </div>
    <div class="benefits-right">
      <div class="benefit-item">
        <div class="logo-container">
          <img
            src="../../assets/svgs/competition.svg"
            loading="lazy"
            class="competition"
          />
        </div>
        <p>Lomba Senam</p>
      </div>
      <div class="benefit-item">
        <div class="logo-container">
          <img
            src="../../assets/svgs/dancing.svg"
            alt="konawa aerobic"
            loading="lazy"
            class="aerobic"
          />
        </div>
        <p>Senam Aerobic</p>
      </div>
      <div class="benefit-item">
        <div class="logo-container">
          <img
            src="../../assets/svgs/holiday.svg"
            alt="liburan bersama konawa"
            loading="lazy"
            class="holiday"
          />
        </div>
        <p>Liburan Bersama</p>
      </div>
    </div>
  </div>
</template>
<style scoped>
.benefit-head {
  text-align: center;
  color: var(--lighten-black);
}
.image-background, .middle-image-background {
  background-image: url("../../assets/images/red-paint-bg.png");
  background-position: center;
  background-size: contain;
  background-repeat: no-repeat;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.benefit-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.benefits-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.benefits-left,
.benefits-right {
  display: flex;
  flex-direction: column;
}
.benefit-item {
  display: flex;
  align-items: center;
}
.benefit-item p {
  color: #624f51;
}
.logo-container {
  background-color: rgba(210, 0, 26, 0.3);
  display: flex;
  justify-content: center;
  align-items: center;
}

@media (min-width: 1024px) {
  .image-background {
    display: none;
  }
  .middle-image-background {
    width: 500px;
  }
  .benefit-img {
    width: 500px;
    border-radius: 20px;
  }
  .benefits-container {
    justify-content: space-around;
  }
  .logo-container {
    width: 75px;
    height: 65px;
    border-radius: 8px;
  }
  .benefits-right .benefit-item {
    flex-direction: row-reverse;
  }
  .benefits-left, .benefits-right {
    gap: 20px;
  }
  .benefit-item {
    gap: 12px;
  }
  .benefit-item p {
    font-size: 18px;
  }
  .poundfit {
    width: 63px;
  }
  .zumba {
    width: 68px;
  }
  .community {
    width: 54px;
  }
  .competition {
    width: 61px;
  }
  .aerobic {
    width: 50.5px;
  }
  .holiday {
    width: 54px;
  }
}

@media (min-width: 501px) and (max-width: 1023px) {
  .middle-image-background {
    display: none;
  }
  .image-container {
    width: 500px;
    height: 350px;
    margin-block: 32px;
  }
  .benefits-container {
    justify-content: space-around;
  }
  .benefits-left, .benefits-right {
    gap: 20px;
  }
  .benefit-item {
    gap: 12px;
  }
  .benefit-item p {
    font-size: 20px;
    font-weight: 600;
  }
  .logo-container {
    width: 75px;
    height: 65px;
    border-radius: 8px;
  }
  .benefit-img {
    border-radius: 16px;
  }
  .poundfit {
    width: 63px;
  }
  .zumba {
    width: 68px;
  }
  .community {
    width: 54px;
  }
  .competition {
    width: 61px;
  }
  .aerobic {
    width: 50.5px;
  }
  .holiday {
    width: 54px;
  }
}

@media (max-width: 500px) {
  .benefit-head {
    font-size: 24px;
    line-height: 1.4;
    margin-top: 40px;
    margin-bottom: 32px;
  }
  .middle-image-background {
    display: none;
  }
  .image-background {
    margin-bottom: 28px;
  }
  .image-container {
    width: 280px;
    height: 200px;
    margin-block: 20px;
  }
  .benefit-img {
    border-radius: 15px;
  }
  .benefits-container {
    padding-inline: 8px;
  }
  .benefits-left,
  .benefits-right {
    gap: 28px;
  }
  .logo-container {
    width: 55px;
    height: 44.5px;
    border-radius: 5px;
  }
  .benefit-item {
    font-size: 14px;
    gap: 10px;
  }
  .poundfit {
    width: 43px;
  }
  .zumba {
    width: 48px;
  }
  .community {
    width: 34px;
  }
  .competition {
    width: 41px;
  }
  .aerobic {
    width: 30.5px;
  }
  .holiday {
    width: 34px;
  }
}
</style>
