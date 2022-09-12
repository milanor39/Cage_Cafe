<template>
    <h2>Menu</h2>
    <section id="coffee">
        <div class="container">
            <CoffeeSection></CoffeeSection>
        </div>
    </section>
    <section id="tea">
        <div class="container">
            <TeaSectionVue></TeaSectionVue>
        </div>
    </section>
    <section id="light meal">
        <div class="container">
          <div class="menu-content">
            <div class="section-title">
              <h2>輕食</h2>
              <p>LIGHT MEAL</p>
            </div>
            <ul>
              <MenuSectionVue v-for="lightMeal in lightMeals" :key="lightMeal.id" v-bind="lightMeal"></MenuSectionVue>
            </ul>
          </div>
        </div>
    </section>
    <section id="dessert">
        <div class="container">
            <div class="menu-content">
              <div class="section-title">
                  <h2>甜點</h2>
                  <p>DESSERT</p>
              </div>
              <ul>
                <MenuSectionVue v-for="dessert in desserts" :key="dessert.id" v-bind="dessert"></MenuSectionVue>
              </ul>
            </div>
        </div>
    </section>
</template>

<script>
import CoffeeSection from '@/components/Menu/CoffeeSection.vue'
import TeaSectionVue from '@/components/Menu/TeaSection.vue'
import MenuSectionVue from '@/components/Menu/MenuSection.vue'

export default {
  data () {
    return {
      lightMeals: [
        {
          id: 'm001',
          name: '番茄義大利麵',
          price: 230,
          img: 'https://girlydrop.com/wp-content/uploads/post/p511.jpg'
        },
        {
          id: 'm002',
          name: '起司漢堡',
          price: 250,
          img: 'https://drive.google.com/uc?export=download&id=1PUL3SxiKh1QJZ4CJN2V6sZEDnbzgW8U-'
        },
        {
          id: 'm003',
          name: '酪梨鮮蝦三明治',
          price: 280,
          img: 'https://drive.google.com/uc?export=download&id=1PZibMb_vDO7tjSlOgkDgIlETdRz_Y6jH'
        },
        {
          id: 'm004',
          name: '楓糖鬆餅',
          price: 220,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/OG458A8096.jpg.webp?d=1420'
        },
        {
          id: 'm005',
          name: '奶油水果鬆餅',
          price: 220,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/nichinanIMGL9210.jpg.webp?d=1420'
        }
      ],
      desserts: [
        {
          id: 'd001',
          name: '水果丹麥麵包',
          price: 70,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ellycollection060.jpg.webp?d=1420'
        },
        {
          id: 'd002',
          name: '草莓奶油蛋糕',
          price: 80,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/mizuho4141396IMG_7893.jpg.webp?d=1420'
        },
        {
          id: 'd003',
          name: '起司蛋糕',
          price: 80,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ogasuta458A8136.jpg.webp?d=1420'
        },
        {
          id: 'd004',
          name: '蒙布朗',
          price: 100,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/MOK_monburancake.jpg.webp?d=1420'
        }
      ]
    }
  },
  components: {
    CoffeeSection,
    TeaSectionVue,
    MenuSectionVue
  }
}
</script>

<style lang="scss">
  .container{
    max-width: 1200px;
    padding-top: 5px;
    padding-bottom: 5px;
  }
  section{
    padding: 20px 0 20px 0;
  }
  h2{
    text-align: center;
  }
  .menu-content{
    ul{
      display: grid;
      grid-template-columns: 1fr 1fr 1fr 1fr;
      gap: 15px;
      padding: 0 10px;
      list-style: none;
      li{
        .lightmeal-card{
          margin-bottom: 10px;
          img{
            max-width: 100%;
          }
          p{
            font-weight: bold;
            font-size: 1.2rem;
            margin: 7px 0;
          }
        }
      }
    }
  }
</style>
