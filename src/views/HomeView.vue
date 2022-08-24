<template>
  <SwiperComponent></SwiperComponent>
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import SwiperComponent from '@/components/SwiperComponent.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    SwiperComponent
  }
}
</script>
