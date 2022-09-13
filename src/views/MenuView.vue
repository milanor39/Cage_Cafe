<template>
  <div class="container">
    <div class="title-background">
      <p>Menu</p>
    </div>
  </div>
  <section id="coffee" class="section-brown">
    <div class="container">
      <div class="menu-content">
        <div class="section-title">
          <h2>咖啡</h2>
          <p>COFFEE</p>
        </div>
        <ul>
          <MenuSectionVue v-for="coffee in coffees" :key="coffee.id" v-bind="coffee"></MenuSectionVue>
        </ul>
      </div>
    </div>
  </section>
  <section id="tea">
    <div class="container">
      <div class="menu-content">
        <div class="section-title">
          <h2>茶 & 其他</h2>
          <p>TEA & OTHER DRINK</p>
        </div>
        <ul>
          <MenuSectionVue v-for="tea in teas" :key="tea.id" v-bind="tea"></MenuSectionVue>
        </ul>
      </div>
    </div>
  </section>
  <section id="light meal" class="section-brown">
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
import MenuSectionVue from '@/components/Menu/MenuSection.vue'

export default {
  data () {
    return {
      coffees: [
        {
          id: 'c001',
          name: '黑咖啡',
          price: 90,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ogasuta458A8143.jpg.webp?d=1420'
        },
        {
          id: 'c002',
          name: '卡布奇諾',
          price: 100,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ogasuta458A8165.jpg.webp?d=1420'
        },
        {
          id: 'c003',
          name: '拿鐵',
          price: 100,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ogasutaFJ02.jpg.webp?d=1420'
        },
        {
          id: 'c004',
          name: '義式濃縮',
          price: 100,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/DSCF9095-Edit.jpg.webp?d=1420'
        }
      ],
      teas: [
        {
          id: 't001',
          name: '紅茶',
          price: 80,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/21ellyri529B.jpg.webp?d=1420'
        },
        {
          id: 't002',
          name: '玫瑰花茶',
          price: 130,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ellycollection074.jpg.webp?d=1420'
        },
        {
          id: 't003',
          name: '珍珠奶茶',
          price: 100,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/tapiocaGFVL5166.jpg.webp?d=1420'
        },
        {
          id: 't004',
          name: '檸檬蘇打',
          price: 110,
          img: 'https://girlydrop.com/wp-content/uploads/post/p880.jpg'
        }
      ],
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
        },
        {
          id: 'm006',
          name: '菠菜鬆餅',
          price: 200,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/TTBIMGL4691.jpg.webp?d=1420'
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
          id: 'd004ˋ',
          name: '胡蘿蔔蛋糕',
          price: 130,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/tachiaraiIMGL4771.jpg.webp?d=1420'
        },
        {
          id: 'd005',
          name: '馬卡龍',
          price: 130,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/PAK75_yoridorimakaron20140304.jpg.webp?d=1420'
        },
        {
          id: 'd006',
          name: '原味甜甜圈',
          price: 110,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/220en458A5555.jpg.webp?d=1420'
        },
        {
          id: 'd007',
          name: '巧克力甜甜圈',
          price: 120,
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/donatsu20160715155804.jpg.webp?d=1420'
        }
      ]
    }
  },
  components: {
    MenuSectionVue
  }
}
</script>

<style lang="scss">
.container {
  max-width: 1200px;
  padding-top: 5px;
  padding-bottom: 5px;
}

section {
  padding: 20px 0 20px 0;
}

.title-background {
  height: 200px;
  background-image: url(https://pakutaso.cdn.rabify.me/shared/img/thumb/cafe201261763.jpg.webp?d=1420);
  background-size: cover;
  background-position: center;
  margin: 20px 0;
  display: flex;
  justify-content: center;
  p{
    font-family: "Playfair Display", serif;
    align-items: center;
    font-size: 3.5rem;
    font-weight: bold;
    color: white;
    letter-spacing: 0.5rem;
  }
}

h2 {
  text-align: center;
}

.menu-content {
  ul {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    gap: 15px;
    padding: 0 10px;
    list-style: none;
    li {
      .lightmeal-card {
        img {
          max-width: 100%;
        }

        p {
          font-weight: bold;
          font-size: 1.2rem;
          margin: 7px 0;
          text-align: center;
        }
      }
    }
  }
}

@media(max-width: 767px){
  .menu-content {
    ul {
      grid-template-columns: 1fr 1fr;
    }
  }
}
@media(max-width: 576px){
  .menu-content {
    ul {
      grid-template-columns: 1fr;
    }
  }
}
</style>
