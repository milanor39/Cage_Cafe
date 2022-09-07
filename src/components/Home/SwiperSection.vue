<template>
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
        <img :src= "eventImg1" alt="">
      </swiper-slide>
      <swiper-slide>
        <img :src="eventImg2" alt="">
      </swiper-slide>
      <swiper-slide>
        <img :src="eventImg3" alt="">
      </swiper-slide>
      <swiper-slide>
        <img :src="eventImg4" alt="">
      </swiper-slide>
      <swiper-slide>
        <img :src="eventImg5" alt="">
      </swiper-slide>
  </swiper>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue'

// Import Swiper styles
import 'swiper/css'

import 'swiper/css/pagination'

// import required modules
import { Autoplay, Pagination } from 'swiper'

export default {
  data () {
    return {
      eventImg1: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/PKU4161369PAR58481.jpg.webp?d=1420',
      eventImg2: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ogasuta458A7885.jpg.webp?d=1420',
      eventImg3: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/E146_iceteatoraimunojinjya.jpg.webp?d=1420',
      eventImg4: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ogasuta458A8104.jpg.webp?d=1420',
      eventImg5: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ellycollection051.jpg.webp?d=1420'
    }
  },
  components: {
    Swiper,
    SwiperSlide
  },
  setup () {
    return {
      modules: [Autoplay, Pagination]
    }
  }
}
</script>

<style lang="scss">
  .swiper {
  width: 100%;
  max-height: 480px;
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
