<template>
  <div class="shop-title">
    <h2>門市資訊</h2>
    <span>Store information</span>
  </div>
  <ul>
    <li v-for="store in storeList" :key="store.name">
      <div class="store-card">
        <div class="card-content">
          <h3>{{store.name}}</h3>
          <p>{{store.address}}</p>
          <p>{{store.tel}}</p>
          <router-link to="/about">詳細資訊</router-link>
        </div>
        <div class="card-img">
          <img :src="store.img" :alt="store.name">
        </div>
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  data () {
    return {
      storeList: [
        {
          name: 'CageCafe東京澀谷本店',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/PAS00164.jpg.webp?d=1420',
          address: '東京都渋谷区代官山町20番20号',
          tel: '0457634930'
        },
        {
          name: 'CageCafe大安店',
          img: 'https://www.photock.jp/photo/middle_webp/photo0000-6368.webp',
          address: '臺北市大安區延吉街35號',
          tel: '028765190'
        },
        {
          name: 'CageCafe內湖店',
          img: 'https://www.photock.jp/photo/middle_webp/photo0000-4115.webp',
          address: '臺北市內湖區康樂街32號',
          tel: '022533382'
        },
        {
          name: 'CageCafe北屯店',
          img: 'https://www.photock.jp/photo/middle_webp/photo0000-2689.webp',
          address: '臺中市北屯區三甲路3號',
          tel: '04519356'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
  .shop-title{
    text-align: center;
    color: black;
  }
  ul{
    padding-left: 0;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 15px;
    list-style: none;
    .store-card{
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-template-rows: 190px;
      .card-content{
        background-color: var(--main-white);
        padding: 0 15px 15px 15px;
        h3{
          font-size: 1.25rem;
          border-bottom: 2px solid var(--main-brown);
          padding-bottom: 3px;
        }
      }
      .card-img{
        object-fit: cover;
        overflow: hidden;
        img{
          max-width: 100%;
        }
      }
    }
  }
</style>
