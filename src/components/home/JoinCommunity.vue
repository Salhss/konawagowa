<script>
import "@/assets/colors.css";
export default {
  name: "join-community",
};
</script>

<template>
  <div class="promote-container">
    <div class="image-container">
      <img
        src="../../assets/images/promote-join.jpeg"
        loading="lazy"
        alt="ikut komunitas konawa hanya Rp. 3000"
      />
    </div>
    <div class="promote-text">
      <div class="tagline">
        <h1>
          Rasakan Berbagai Keseruan<br />Bersama Kami Dengan Harga<br />Terjangkau
          !
        </h1>
      </div>
      <div class="price-text">
        <h1>Mulai dari</h1>
        <div class="price">
          <h1>Rp. 3000</h1>
          <div class="underline"></div>
        </div>
      </div>
      <div class="description">
        <p>
          Dapatkan informasi terikini mengenai aktifitas terbaru dan terlengkap
          Konawa Gowa
        </p>
      </div>
      <div class="btn-container">
        <div class="action-btn">
          <p>Gabung Sekarang!</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.promote-container {
  display: flex;
  padding-inline: 20px;
}
.tagline h1 {
  color: #a60015;
}
.price-text {
  display: flex;
}
.price-text > h1 {
  color: #545454;
  text-align: left;
}
.price h1 {
  color: var(--red-default);
}
.price {
    display: flex;
    flex-direction: column;
  }
.underline {
  background-color: var(--yellow);
  width: 100%;
}
.description p {
  color: #545454;
  margin: 0;
}
.action-btn {
  background-color: var(--red);
  color: var(--white);
  font-weight: 700;
  text-align: center;
  width: fit-content;
  cursor: pointer;
}
.action-btn:hover {
    background-color: var(--red-default);
}

@media (min-width: 1024px) {
    .promote-container {
    flex-direction: row-reverse;
    justify-content: space-around;
    align-items: center;
    padding-inline: 20px;
    margin-top: 80px;
    margin-bottom: 40px;
  }
  .image-container {
    width: 600px;
    height: 420px;
    display: flex;
    align-items: center;
  }
  img {
    width: 100%;
    object-fit: cover;
    border-radius: 15px;
  }
  .tagline h1 {
    margin-bottom: 0px;
  }
  .price-text {
    gap: 12px;
  }
  .price-text h1 {
    font-size: 28px;
    margin-bottom: 4px;
  }
  .underline {
    height: 8px;
  }
  .description {
    margin-top: 20px;
    margin-bottom: 62px;
  }
  .action-btn {
    padding-block: 20px;
    padding-inline: 26px;
    border-radius: 16px;
  }
  .action-btn p {
    font-size: 20px;
    margin: 0px;
  }
}

@media (min-width: 501px) and (max-width: 1023px) {
  h1 {
    font-size: 20px;
  }
  .promote-container {
    flex-direction: row-reverse;
    justify-content: space-around;
    align-items: center;
    padding-inline: 20px;
  }
  .promote-text {
    width: 50%;
  }
  .image-container {
    width: 530px;
    height: 420px;
    display: flex;
    align-items: center;
  }
  img {
    width: 100%;
    object-fit: cover;
    border-radius: 15px;
  }
  .price-text {
    gap: 8px;
  }
  .price h1  {
    margin-bottom: 4px;
  }
  .underline {
    height: 6px;
  }
  .description {
    width: 90%;
    font-size: 14px;
    margin-block: 16px;
  }
  .action-btn {
    padding-inline: 16px;
    padding-block: 12px;
    border-radius: 8px;
  }
  .action-btn p {
    margin: 0;
  }
}

@media (max-width: 500px) {
  .promote-container {
    margin-top: 52px;
    flex-direction: column;
  }
  .image-container {
    width: 330px;
    height: 220px;
    align-self: center;
  }
  img {
    width: 100%;
    object-fit: cover;
    border-radius: 15px;
  }
  .tagline h1 {
    font-size: 24px;
    margin-bottom: 0;
  }
  .price-text h1 {
    font-size: 24px;
  }
  .price-text {
    gap: 8px;
  }
  .price h1 {
    margin-bottom: 5px;
  }
  .underline {
    height: 4px;
    background-color: #e3c500;
  }
  .description p {
    margin-top: 12px;
  }
  .btn-container {
    display: flex;
    justify-content: center;
    margin-top: 28px;
  }
  .action-btn {
    border-radius: 5px;
  }
  .action-btn p {
    padding-inline: 19px;
  }
}
</style>
