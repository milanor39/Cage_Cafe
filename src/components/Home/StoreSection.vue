<template>
  <div class="section-title">
    <h2>門市資訊</h2>
    <p>STORE</p>
  </div>
  <div class="shop-area">
    <div class="shop-content">
      <router-link to="/store">
        <h2>尋找CageCafe</h2>
      </router-link>
    </div>
  </div>
</template>

<style lang="scss">
  .shop-area{
    padding: 0 10px;
    .shop-content{
      background-image: url(https://pakutaso.cdn.rabify.me/shared/img/thumb/ogasutaFJ04.jpg.webp?d=1420);
      background-size: cover;
      background-position: center;
      height: 300px;
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 16px 0;
      a{
        background-color: rgba($color: white, $alpha: 1);
        color: var(--main-brown);
        text-decoration: none;
        transition-duration: 00.3s;
        padding: 0 20px;
      }
      a:hover{
        background-color: rgba($color: white, $alpha: 0.6);
      }
    }
  }
  @media (max-width: 767px){
    .shop-area{
      .shop-content{
        height: 200px;
      }
    }
  }
</style>
