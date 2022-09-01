<template>
  <div class="menu-title">
    <h2>菜單一覽</h2>
    <p>MENU</p>
  </div>
  <div class="menu-list">
    <ul>
      <li v-for="item in menucard" :key="item.engtitle">
        <router-link to="/about">
          <div class="list-card">
            <img :src="item.img" :alt="item.engtitle">
            <div class="card-title">
              <h3>{{item.title}}</h3>
            </div>
          </div>
        </router-link>
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
      menucard: [
        {
          title: '餐點',
          engtitle: 'Food',
          img: 'https://www.pakutaso.com/shared/img/thumb/MOK_monburancake_TP_V.jpg'
        },
        {
          title: '飲品',
          engtitle: 'Drink',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ellycollection044.jpg.webp?d=1420'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
.menu-title{
  text-align: center;
  color: var(--main-black);
  h2{
    margin: 0;
    font-size: 1.8rem;
  }
  p{
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem;
    margin: 0 0 5px 0;
  }
  border-bottom: 1px solid var(--main-black);
}
.menu-list{
  margin: 0 auto;
  ul{
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: auto;
    gap: 15px;
    padding: 0 10px;
    list-style: none;
    li{
      transition-duration: 0.3s;
      .list-card{
        position: relative;
        height: 300px;
        overflow: hidden;
        img{
          max-width: 100%;
        }
        .card-title{
          position: absolute;
          top: 0;
          left: 30px;
          color: white;
          font-size: 2rem;
        }
      }
    }
    li:hover{
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
@media (max-width: 767px){
  .menu-list{
    ul{
      grid-template-columns: 1fr;
    }
  }
}
</style>
