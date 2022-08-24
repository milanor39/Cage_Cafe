<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
  <img src="https://pakutaso.cdn.rabify.me/shared/img/thumb/NKJ56_coffeecok.jpg.webp?d=1420" alt="">
  <img src="https://pakutaso.cdn.rabify.me/shared/img/thumb/NKJ56_coffeecok.jpg.webp?d=1420" alt="">
  <img src="https://pakutaso.cdn.rabify.me/shared/img/thumb/NKJ56_coffeecok.jpg.webp?d=1420" alt="">
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>
