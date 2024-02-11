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
</template>
<style scoped>
.benefit-head {
  text-align: center;
  color: var(--lighten-black);
}
.image-background {
  background-image: url("../../assets/images/red-paint-bg.png");
  background-position: center;
  background-size: cover;
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

@media (max-width: 500px) {
  .benefit-head {
    font-size: 24px;
    line-height: 1.4;
    margin-top: 40px;
    margin-bottom: 32px;
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
}
</style>
