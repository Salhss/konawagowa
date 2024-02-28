<script>
import "@/assets/colors.css";
export default {
  name: "Galery",
};
</script>
<template>
  <section class="galery">
    <h1>Jadilah Bagian dari Konawa</h1>
    <p>
      Ikuti berbagai aktivitas kami, dan dapatkan keseruan dengan komunitas yang
      luas dengan harga terjangkau
    </p>

    <div class="images-container">
      <div class="images">
        <img
          src="../../assets/images/galery/image5.jpg"
          width="530"
          height="250"
          loading="lazy"
          alt="konawa gowa"
        />
        <img
          src="../../assets/images/galery/image6.jpg"
          width="530"
          height="250"
          loading="lazy"
          alt="konawa gowa"
        />
        <img
          src="../../assets/images/galery/image7.jpg"
          width="530"
          height="250"
          loading="lazy"
          alt="konawa gowa"
        />
        <img
          src="../../assets/images/galery/image8.jpg"
          width="530"
          height="250"
          loading="lazy"
          alt="konawa gowa"
        />
      </div>
      <div class="images">
        <img
          src="../../assets/images/galery/image1.jpg"
          width="530"
          height="250"
          loading="lazy"
          alt="konawa gowa"
        />
        <img
          src="../../assets/images/galery/image2.jpg"
          width="530"
          height="250"
          loading="lazy"
          alt="konawa gowa"
        />
        <img
          src="../../assets/images/galery/image3.jpg"
          width="530"
          height="250"
          loading="lazy"
          alt="konawa gowa"
        />
        <img
          src="../../assets/images/galery/image4.jpg"
          width="530"
          height="250"
          loading="lazy"
          alt="konawa gowa"
        />
      </div>
    </div>
  </section>
</template>
<style scoped>
.galery {
  margin-top: 80px;
}

h1,
p {
  color: var(--lighten-black);
  text-align: center;
}

.images-container {
  overflow-x: auto;
}

.images {
  display: flex;
  align-items: center;
}

img {
    object-fit: cover;
  }

@media (min-width: 1021px) {
  .galery {
    padding-inline: 40px;
  }
  h1 {
    font-size: 32px;
  }
  p {
    font-size: 20px;
  }
  .images-container {
    margin-top: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
  }
  .images {
    gap: 16px;
    margin-bottom: 16px;
  }

  img {
    width: 250px;
    height: 180px;
    border-radius: 20px;
  }
 
}
@media (min-width: 761px) and (max-width: 1020px) {
  .images-container {
    margin-top: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
  }
  .images {
    gap: 16px;
    margin-bottom: 16px;
  }

  img {
    width: 160px;
    height: 130px;
    border-radius: 12px;
  }
}
@media (max-width: 760px) {
  p {
    font-size: 14px;
  }

  .images {
    gap: 20px;
    margin-bottom: 20px;
  }

  img {
    width: 153px;
    height: 124px;
    border-radius: 15px;
  }
}
</style>
