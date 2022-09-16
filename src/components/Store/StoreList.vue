<template>
    <li class="store">
        <div class="store-card">
            <div class="img-box">
                <img :src="img" :alt="name">
            </div>
            <div class="store-content">
                <h3>{{name}}</h3>
                <ul>
                    <li>地址： {{address}}</li>
                    <li>電話： {{tel}}</li>
                    <li>營業時間： {{businessHours}}</li>
                </ul>
                <a href="#">詳細資訊</a>
            </div>
        </div>
    </li>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true
    },
    address: {
      type: String,
      required: true
    },
    img: {
      type: String,
      required: true
    },
    tel: {
      type: String,
      required: true
    },
    businessHours: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="scss">
    .store{
        margin-bottom: 20px;
    }
    .store-card{
        display: flex;
        background-color: var(--main-white);
        padding: 10px;
        .store-content{
            padding: 0 0 40px 40px;
            ul{
                padding: 0;
                margin-bottom: 30px;
                li{
                    line-height: 2rem;
                }
            }
            a{
                background-color: var(--main-brown);
                color: var(--main-white);
                text-decoration: none;
                padding: 10px 20px;
                border: 1px solid var(--main-brown);
            }
            a:hover{
                background-color: var(--section-brown);
                color: var(--main-brown);
            }
        }
        .img-box{
            max-width: 400px;
            display: flex;
            align-items: center;
            img{
                width: 100%;
            }
        }
    }
    @media(max-width: 767px){
        .store-card{
            display: block;
            margin: 0 auto;
            .img-box{
                margin: 0 auto;
            }
            ul{
                padding-left: 0;
            }
        }
    }
</style>
