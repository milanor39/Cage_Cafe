<template>
  <div class="menu-title">
    <h2>推薦餐點&飲品</h2>
    <p>Recommened Dishes & Drinks</p>
  </div>
  <div class="menu-list">
    <ul>
        <li v-for="dish in recommenedDishes" :key="dish.name">
          <div class="list-card">
            <router-link to="/about">
              <img :src="dish.img" :alt="dish.name">
              <span>HOT</span>
              <h3>{{dish.name}}</h3>
            </router-link>
          </div>
        </li>
      </ul>
  </div>
  <div class="menu-seemore">
    <router-link to="/about">看更多</router-link>
  </div>
</template>

<script>
export default {
  data () {
    return {
      recommenedDishes: [
        {
          name: '特製柳橙塔',
          img: 'https://drive.google.com/uc?export=download&id=1-br3i2SUYhDgwfgJ55SWcQfTRNbsXPOi'
        },
        {
          name: '招牌番茄肉醬麵',
          img: 'https://girlydrop.com/wp-content/uploads/post/p511.jpg'
        },
        {
          name: '招牌卡布奇諾',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ogasuta458A8165.jpg.webp?d=1420'
        },
        {
          name: '蜂蜜牛奶拿鐵',
          img: 'https://girlydrop.com/wp-content/uploads/post/p538.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
.menu-title{
  text-align: center;
  color: var(--main-brown);
  h2{
    margin: 0;
  }
}
.menu-list{
  ul{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    grid-template-rows: auto;
    gap: 15px;
    padding: 0 10px;
    list-style: none;
    .list-card{
      position: relative;
      overflow: hidden;
      transition-duration: 0.3s;
      display: flex;
      img{
        max-width: 100%;
        vertical-align: middle;
      }
      span{
        position: absolute;
        top: -8px;
        left: -38px;
        color: azure;
        background-color: rgba($color: #ff1515, $alpha: 0.6);
        padding:25px 40px 5px 40px;
        transform: rotate(-45deg);
        font-size: 1.1em;
      }
      h3{
        color: var(--main-white);
        position: absolute;
        top: 140px;
        left: 10px;
      }
    }
    .list-card:hover{
      box-shadow: 0 0 5px 5px var(--main-brown);
      opacity: 0.7;
    }
  }
}
.menu-seemore{
  text-align: center;
  a{
    color: var(--main-black);
    font-weight: bold;
    font-size: 1.2rem;
    transition: 0.3s ease-out;
    border-bottom: 2px solid white;
    text-decoration: none;
    padding: 0 30px;
  }
}
.menu-seemore:hover a{
  border-bottom: 2px solid var(--main-black);
}
@media (max-width: 1200px){
  .menu-list{
    ul{
      grid-template-columns: 1fr 1fr;
    }
  }
}
</style>
