<template>
    <div class="btn-container">
      <p>Join Komunitas Kami</p>
    </div>
</template>
<script>
export default {
    name: 'join-button'
}
</script>
<style scoped>

 .btn-container {
    background-color: var(--red);
    color: var(--white-gray);
    font-weight: 700;
    padding-inline: 18px;
    border-radius: 5px;
    box-shadow: 0px 4px  4px rgba(0, 0, 0, 0.25);
    cursor: pointer;
    transition: all 200ms ease-in;
  }
  .btn-container:hover {
    box-shadow: none;
  }

  @media (min-width: 1400px) {
    .btn-container p {
      font-size: 26px !important;
    }
    .btn-container {
      padding-block: 20px !important;
      padding-inline: 25px;
    }
  }
  @media (min-width: 913px) {
    .btn-container {
      padding-block: 15px;
    }
    .btn-container p {
      font-size: 18px;
    }
  }
  @media (min-width: 700px) {
    .btn-container {
        transform: scale(0.8);
        width: 100%;
        height: 100%;
        display: flex;
        align-items: center;
    }
    p {
        margin: 0;
    }
  }
</style>