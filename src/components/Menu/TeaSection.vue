<template>
    <div class="section-title">
        <h2>茶 & 其他</h2>
        <p>TEA & OTHER DRINK</p>
    </div>
    <div class="section-content">
        <div class="tea-content">
            <ul>
                <li v-for="tea in teaList" :key="tea.engName">
                    <div class="tea-card">
                        <img :src="tea.img" :alt="tea.name">
                        <p>{{tea.name}}</p>
                        <span>{{tea.price}}</span>
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
      teaList: [
        {
          name: '紅茶',
          engName: 'Black Tea',
          price: '$80',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/21ellyri529B.jpg.webp?d=1420'
        },
        {
          name: '玫瑰花茶',
          engName: 'Rose Tea',
          price: '$130',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/ellycollection074.jpg.webp?d=1420'
        },
        {
          name: '珍珠奶茶',
          engName: 'Bubble Tea',
          price: '$100',
          img: 'https://pakutaso.cdn.rabify.me/shared/img/thumb/tapiocaGFVL5166.jpg.webp?d=1420'
        },
        {
          name: '檸檬蘇打',
          engName: 'Lemon Squash',
          price: '$110',
          img: 'https://girlydrop.com/wp-content/uploads/post/p880.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
    .tea-content{
        ul{
            display: grid;
            grid-template-columns: 1fr 1fr 1fr 1fr;
            gap: 15px;
            padding: 0 10px;
            list-style: none;
            li{
                .tea-card{
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
