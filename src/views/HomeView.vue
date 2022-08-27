<template>
  <section>
      <div class="container">
        <SwiperComponent></SwiperComponent>
      </div>
  </section>
  <section class="section-news">
    <div class="container">
      <NewsComponent></NewsComponent>
    </div>
  </section>
  <section>
    <div class="container">
      <MenuComponent></MenuComponent>
    </div>
  </section>
  <section class="hellovue">
    <div class="container">
      <HelloWorld msg="Welcome to Your Vue.js App"/>
    </div>
  </section>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import SwiperComponent from '@/components/Home/SwiperComponent.vue'
import NewsComponent from '@/components/Home/NewsComponent.vue'
import MenuComponent from '@/components/Home/MenuComponent.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    SwiperComponent,
    NewsComponent,
    MenuComponent
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
  .section-news,.hellovue{
    background-color: var(--section-brown);
  }
</style>
