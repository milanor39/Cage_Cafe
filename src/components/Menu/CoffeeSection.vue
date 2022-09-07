<template>
    <div class="section-title">
        <h2>咖啡</h2>
        <p>COFFEE</p>
    </div>
    <div class="section-content">
        <div class="coffee-content">
            <ul>
                <li v-for="coffee in coffeeList" :key="coffee.engName">
                    <div class="coffee-card">
                        <img :src="coffee.img" :alt="coffee.name">
                        <p>{{coffee.name}}</p>
                        <span>{{coffee.price}}</span>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
  data () {
    return {
      coffeeList: [
        {
          name: '黑咖啡',
          engName: 'Black Coffee',
          price: '$90',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ogasuta458A8143.jpg.webp?d=1420'
        },
        {
          name: '冰咖啡',
          engName: 'Ice Coffee',
          price: '90',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/PP_coffetime.jpg.webp?d=1420'
        },
        {
          name: '卡布奇諾',
          engName: 'Cappuccino',
          price: '$100',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ogasuta458A8165.jpg.webp?d=1420'
        },
        {
          name: '拿鐵',
          engName: 'Latte',
          price: '$100',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ogasutaFJ01.jpg.webp?d=1420'
        },
        {
          name: '義式濃縮',
          engName: 'Espresso',
          price: '$100',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/DSCF9095-Edit.jpg.webp?d=1420'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
    .coffee-content{
        ul{
            display: grid;
            grid-template-columns: 1fr 1fr 1fr 1fr;
            gap: 15px;
            padding: 0 10px;
            list-style: none;
            li{
                .coffee-card{
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
