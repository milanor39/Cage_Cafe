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
        <HelloWorld msg="Welcome to Your Vue.js App"/>
      </div>
    </section>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import SwiperComponent from '@/components/Home/SwiperComponent.vue'
import NewsComponent from '@/components/Home/NewsComponent.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    SwiperComponent,
    NewsComponent
  }
}
</script>

<style lang="scss">
  :root{
    --section-bg: #B9887D;
  }
  .container{
    max-width: 1200px;
    padding-top: 5px;
    padding-bottom: 5px;
  }
  .section-news{
    background-color: var(--section-bg);
  }
</style>
