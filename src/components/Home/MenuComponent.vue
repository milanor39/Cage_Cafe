<template>
  <div class="title">
    <h2>推薦餐點&飲品</h2>
    <p>Recommened Dishes & Drinks</p>
    <div class="dish-list">
          <ul>
            <li v-for="dish in recommenedDishes" :key="dish.name">
              <div class="list-card">
                <img :src="dish.img" :alt="dish.name">
                <h3>{{dish.name}}</h3>
              </div>
            </li>
          </ul>
        </div>
    <router-link class="seemore" to="/about">看更多</router-link>
  </div>
</template>

<script>
export default {
  data () {
    return {
      recommenedDishes: [
        {
          name: '綜合水果鬆餅',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/nichinanIMGL9207.jpg.webp?d=1420'
        },
        {
          name: '和風義大利麵',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/IK21317929.jpg.webp?d=1420'
        },
        {
          name: '卡布奇諾',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ogasuta458A8165.jpg.webp?d=1420'
        },
        {
          name: '錫蘭紅茶',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/07ellyri529B.jpg.webp?d=1420'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
.title{
  .dish-list{
    ul{
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 15px;
      padding: 0 10px;
      list-style: none;
      .list-card{
        position: relative;
        img{
          max-width: 100%;
          border-radius: 15px;
        }
        h3{
          position: absolute;
          top: 0;
          left: 10px;
        }
      }
    }
  }
}
</style>
