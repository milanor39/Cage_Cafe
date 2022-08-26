<template>
  <div class="title">
    <h2>最新消息</h2>
    <p>NEWS</p>
    <ul class="newslist">
      <li v-for="news in newslist" :key="news.title">
        <router-link to="/about">
          <div>
            <img :src="news.img" alt="">
          </div>
          <h3>{{news.title}}</h3>
          <small>{{news.date}}</small>
        </router-link>
      </li>
    </ul>
    <router-link class="seemore" to="/about">看更多</router-link>
  </div>
</template>

<script>
export default {
  data () {
    return {
      newslist: [
        {
          title: '秋季新品上市',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/kissaten-_92A9197-8916.jpg.webp?d=1420',
          date: '2023/11/25'
        },
        {
          title: '2023中秋禮盒預購中',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ellysakuramc14.jpg.webp?d=1420',
          date: '2023/8/30'
        },
        {
          title: '外帶飲品限時優惠',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ellycollection051.jpg.webp?d=1420',
          date: '2023/7/10'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
  .title{
    text-align: center;
    h2{
      margin: 0;
    }
    .newslist{
      display:grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 20px;
      padding: 0 10px;
      list-style: none;
      li{
        background-color: var(--main-white);
        border-radius: 10px;
        transition-duration: 0.3s;
        a{
          display: block;
          text-decoration: none;
          padding-bottom: 18px;
          img{
            max-width: 100%;
            border-radius: 10px 10px 0 0;
          }
          h3{
            margin-bottom: 0;
            font-size: 1.5em;
          }
        }
      }
      li:hover{
        box-shadow: 0 0 5px 5px var(--main-brown);
        opacity: 0.7;
      }
    }
    .seemore{
      color: var(--main-black);
      font-size: 1.2rem;
      font-weight: bold;
      text-decoration: none;
      transition-duration: 0.3s;
    }
    .seemore:hover{
      color: var(--main-white);
    }
  }
</style>
