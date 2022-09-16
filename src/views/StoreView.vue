<template>
   <div class="container">
    <div class="title-background">
      <p>STORE</p>
    </div>
  </div>
  <section class="section-brown">
    <div class="container">
      <div class="store-content">
        <div class="section-title">
          <h2>北部地區</h2>
          <p>North Region</p>
        </div>
        <ul>
          <StoreListVue v-for="store in northRegion" :key="store.id" v-bind="store"></StoreListVue>
        </ul>
      </div>
    </div>
  </section>
  <section>
    <div class="container">
      <div class="store-content">
        <div class="section-title">
          <h2>中部地區</h2>
          <p>Central Region</p>
        </div>
        <ul>
          <StoreListVue v-for="store in centralRegion" :key="store.id" v-bind="store"></StoreListVue>
        </ul>
      </div>
    </div>
  </section>
  <section  class="section-brown">
    <div class="container">
      <div class="store-content">
        <div class="section-title">
          <h2>南部地區</h2>
          <p>South Region</p>
        </div>
        <ul>
          <StoreListVue v-for="store in southRegion" :key="store.id" v-bind="store"></StoreListVue>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
import StoreListVue from '@/components/Store/StoreList.vue'

export default {
  data () {
    return {
      northRegion: [
        {
          id: 'sn001',
          name: '西門店',
          address: '臺北市萬華區昆明街5號',
          img: 'https://www.photock.jp/photo/middle_webp/photo0000-2576.webp',
          tel: '02-82967216',
          businessHours: '07:00-21:00'
        },
        {
          id: 'sn002',
          name: '指南店',
          address: '臺北市文山區指南路5號',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/yokohama320dPAR580852226.jpg.webp?d=1420',
          tel: '02-82967216',
          businessHours: '07:00-21:00'
        },
        {
          id: 'sn003',
          name: '寧波店',
          address: '臺北市中正區寧波西街32號',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/noogata-pakuPAR543822688.jpg.webp?d=1420',
          tel: '02-82967216',
          businessHours: '07:00-21:00'
        }
      ],
      centralRegion: [
        {
          id: 'ss001',
          name: '北屯店',
          address: '臺中市北屯區山西南一街18號',
          img: 'https://www.photock.jp/photo/middle_webp/photo0000-7212.webp',
          tel: '04-83164499',
          businessHours: '07:00-21:00'
        },
        {
          id: 'ss002',
          name: '豐原店',
          address: '臺中市豐原區新生北路20號',
          img: 'https://www.photock.jp/photo/middle_webp/photo0000-3361.webp',
          tel: '04-99850061',
          businessHours: '07:00-21:00'
        }
      ],
      southRegion: [
        {
          id: 'ss001',
          name: '西賢店',
          address: '臺南市中西區西賢街35號',
          img: 'https://www.photock.jp/photo/middle_webp/photo0000-3448.webp',
          tel: '06-2915889',
          businessHours: '07:00-21:00'
        },
        {
          id: 'sn002',
          name: '苓雅店',
          address: '高雄市苓雅區文橫二路19號',
          img: 'https://www.photock.jp/photo/middle_webp/photo0000-4126.webp',
          tel: '07-8050576',
          businessHours: '07:00-21:00'
        },
        {
          id: 'sn003',
          name: '鳳山店',
          address: '高雄市鳳山區南進四街29號',
          img: 'https://www.photock.jp/photo/middle_webp/photo0000-5906.webp',
          tel: '07-9819254',
          businessHours: '07:00-21:00'
        }
      ]
    }
  },
  components: {
    StoreListVue
  }
}
</script>

<style lang="scss">
  li{
    list-style: none;
  }
  .store-content{
    ul{
      padding-left: 0;
    }
  }
</style>
