<template>
  <div class="container">
    <swiper
      :spaceBetween="30"
      :centeredSlides="true"
      :autoplay="{
        delay: 2500,
        disableOnInteraction: false,
      }"
      :pagination="{
        clickable: true,
      }"
      :navigation="true"
      :modules="modules"
      class="mySwiper"
    >
      <swiper-slide>
        <img src="https://pakutaso.cdn.rabify.me/shared/img/thumb/ogasuta458A8068.jpg.webp?d=1420" alt="">
      </swiper-slide>
      <swiper-slide>
        <img src="https://pakutaso.cdn.rabify.me/shared/img/thumb/ogasuta458A7885.jpg.webp?d=1420" alt="">
      </swiper-slide>
      <swiper-slide>
        <img src="https://pakutaso.cdn.rabify.me/shared/img/thumb/E146_iceteatoraimunojinjya.jpg.webp?d=1420" alt="">
      </swiper-slide>
      <swiper-slide>
        <img src="https://pakutaso.cdn.rabify.me/shared/img/thumb/ogasuta458A8104.jpg.webp?d=1420" alt="">
      </swiper-slide>
      <swiper-slide>
        <img src="https://pakutaso.cdn.rabify.me/shared/img/thumb/ellycollection051.jpg.webp?d=1420" alt="">
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue'

// Import Swiper styles
import 'swiper/css'

import 'swiper/css/navigation'
import 'swiper/css/pagination'

// import required modules
import { Autoplay, Pagination, Navigation } from 'swiper'

export default {
  components: {
    Swiper,
    SwiperSlide
  },
  setup () {
    return {
      modules: [Autoplay, Pagination, Navigation]
    }
  }
}
</script>

<style lang="scss">
  .container{
    max-width: 1200px;
  }
  .swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 50%;
  object-fit: cover;
}
</style>
