<template>
  <div class="shop-title">
    <h2>門市資訊</h2>
    <span>Store information</span>
  </div>
  <ul>
    <li v-for="store in storeList" :key="store.name">
      <div class="store-card">
        <div class="card-content">
          <h2>{{store.name}}</h2>
          <p>{{store.address}}</p>
          <p>{{store.tel}}</p>
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
          name: 'CageCafe公館店',
          img: 'https://www.photock.jp/photo/middle_webp/photo0000-6368.webp',
          address: '新潟県十日町市田中町本通り10番30号',
          tel: '00000000'
        },
        {
          name: 'CageCafe公館店',
          img: 'https://www.photock.jp/photo/middle_webp/photo0000-6368.webp',
          address: '新潟県十日町市田中町本通り10番30号',
          tel: '00000000'
        },
        {
          name: 'CageCafe公館店',
          img: 'https://www.photock.jp/photo/middle_webp/photo0000-6368.webp',
          address: '新潟県十日町市田中町本通り10番30号',
          tel: '00000000'
        },
        {
          name: 'CageCafe公館店',
          img: 'https://www.photock.jp/photo/middle_webp/photo0000-6368.webp',
          address: '新潟県十日町市田中町本通り10番30号',
          tel: '00000000'
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
      display: flex;
      justify-content: center;
      .card-content{
        background-color: var(--main-white);
      }
      .card-img{
        img{
          max-width: 100%;
        }
      }
    }
  }
</style>
