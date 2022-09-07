<template>
    <div class="section-title">
        <h2>輕食</h2>
        <p>LIGHT MEAL</p>
    </div>
    <div class="section-content">
        <div class="lightmeal-content">
            <ul>
                <li v-for="lightmeal in lightmealList" :key="lightmeal.engName">
                    <div class="lightmeal-card">
                        <img :src="lightmeal.img" :alt="lightmeal.name">
                        <p>{{lightmeal.name}}</p>
                        <span>{{lightmeal.price}}</span>
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
      lightmealList: [
        {
          name: '番茄義大利麵',
          engName: 'Tomato Spaghetti',
          price: '$230',
          img: 'https://girlydrop.com/wp-content/uploads/post/p511.jpg'
        },
        {
          name: '起司漢堡',
          engName: 'Cheese Burger',
          price: '$250',
          img: 'https://drive.google.com/uc?export=download&id=1PUL3SxiKh1QJZ4CJN2V6sZEDnbzgW8U-'
        },
        {
          name: '酪梨鮮蝦三明治',
          engName: 'Shrimp Sandwich with Avocado',
          price: '$280',
          img: 'https://drive.google.com/uc?export=download&id=1PZibMb_vDO7tjSlOgkDgIlETdRz_Y6jH'
        },
        {
          name: '楓糖鬆餅',
          engName: 'Maple Pancake',
          price: '$220',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/OG458A8096.jpg.webp?d=1420'
        },
        {
          name: '奶油水果鬆餅',
          engName: 'Fruit Pancakes With Fresh Cream',
          price: '$220',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/nichinanIMGL9210.jpg.webp?d=1420'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
    .lightmeal-content{
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
