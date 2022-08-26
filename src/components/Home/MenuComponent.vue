<template>
  <div class="title">
    <h2>菜單一覽</h2>
    <p>MENU</p>
    <div class="popular-drinks">
        <div class="drink-title">
            <h2>{{drink.title}}</h2>
            <p>{{drink.engtitle}}</p>
        </div>
        <div class="drink-img">
            <img :src="drink.img" alt="">
        </div>
    </div>
    <router-link class="seemore" to="/about">看更多</router-link>
  </div>
</template>

<script>
export default {
  data () {
    return {
      drink: {
        title: '熱門飲品',
        engtitle: 'POPULAR DRINKS',
        img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/DSCF9095-Edit.jpg.webp?d=1420'
      }
    }
  }
}
</script>

<style lang="scss">
.title{
  .popular-drinks{
    display: grid;
    grid-template-columns: 1fr 1fr;
    border: 1px solid black;
    .drink-title{
      background-color: var(--main-white);
    }
    img{
        max-width: 100%;
    }
  }
}
</style>
