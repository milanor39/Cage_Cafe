<template>
  <section>
      <div class="container">
        <SwiperComponent></SwiperComponent>
      </div>
  </section>
  <section class="section-brown">
    <div class="container">
      <NewsComponent></NewsComponent>
    </div>
  </section>
  <section>
    <div class="container">
      <MenuComponent></MenuComponent>
    </div>
  </section>
  <section class="section-brown">
    <div class="container">
      <StoreComponent></StoreComponent>
    </div>
  </section>
</template>

<script>
// @ is an alias to /src
import SwiperComponent from '@/components/Home/SwiperComponent.vue'
import NewsComponent from '@/components/Home/NewsComponent.vue'
import MenuComponent from '@/components/Home/MenuComponent.vue'
import StoreComponent from '@/components/Home/StoreComponent.vue'

export default {
  name: 'HomeView',
  components: {
    SwiperComponent,
    NewsComponent,
    MenuComponent,
    StoreComponent
  }
}
</script>

<style lang="scss">
  .container{
    max-width: 1200px;
    padding-top: 5px;
    padding-bottom: 5px;
  }
  section{
    padding: 20px 0 20px 0;
  }
  .section-brown{
    background-color: var(--section-brown);
  }
</style>
