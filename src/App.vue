<template>
  <header>
    <div class="header-content">
      <a class="burger-menu" href="#" @click.prevent="toggleMenu">
        <div class="burger-line"></div>
        <div class="burger-line"></div>
        <div class="burger-line"></div>
      </a>
      <div class="logo">
        <router-link to="/">
          <img src="./assets/logo.png" alt="logo">
          <h1>Cage_Cafe</h1>
        </router-link>
      </div>
      <nav class="pc-menu">
        <ul class="nav-link">
          <li>
            <router-link to="/news">
              <h3>最新消息</h3>
              <span>NEWS</span>
            </router-link>
          </li>
          <li>
            <router-link to="/about">
              <h3>關於我們</h3>
              <span>ABOUT</span>
            </router-link>
          </li>
          <li>
            <router-link to="/menu">
              <h3>菜單一覽</h3>
              <span>MENU</span>
            </router-link>
          </li>
          <li>
            <router-link to="/store">
              <h3>門市資訊</h3>
              <span>STORE</span>
            </router-link>
          </li>
        </ul>
      </nav>
    </div>
    <div class="mobile-menu" v-show="showMenu">
      <ul>
        <li>
          <router-link to="/news">
            <h5 class="mobile-title">最新消息 -<span> NEWS</span></h5>
          </router-link>
        </li>
        <li>
          <router-link to="/about">
            <h5 class="mobile-title">關於CageCafe -<span> ABOUT</span></h5>
          </router-link>
        </li>
        <li>
          <router-link to="/menu">
            <h5 class="mobile-title">菜單一覽 -<span> MENU</span></h5>
          </router-link>
        </li>
        <li>
          <router-link to="/store">
            <h5 class="mobile-title">門市資訊 -<span> STORE</span></h5>
          </router-link>
        </li>
        <li>
          <router-link to="/about">
            <h5 class="mobile-title">聯絡我們 -<span> CONTACT</span></h5>
          </router-link>
        </li>
      </ul>
    </div>
  </header>
  <main>
    <router-view/>
  </main>
  <footer>
    <div class="container">
      <div class="footer-content">
        <div class="sns">
          <ul>
            <li><a href="#" target="_blank"><i class="fa-brands fa-square-facebook fa-2x"></i></a></li>
            <li><a href="#" target="_blank"><i class="fa-brands fa-instagram fa-2x"></i></a></li>
            <li><a href="#" target="_blank"><i class="fa-brands fa-twitter fa-2x"></i></a></li>
          </ul>
        </div>
        <div class="footer-list">
          <ul>
            <li>
              <router-link to="/about">關於CageCafe</router-link>
            </li>
            <li>
              <a href="https://recruit.komeda-coffee.jp/" target="_blank">徵才情報</a>
            </li>
            <li>
              <router-link to="/contact">聯絡我們</router-link>
            </li>
          </ul>
        </div>
      </div>
      <p class="copy"><small>&copy; 2022 CageCafe</small></p>
    </div>
  </footer>
</template>

<script>
export default {
  data () {
    return {
      showMenu: false
    }
  },
  methods: {
    toggleMenu () {
      this.showMenu = !this.showMenu
    }
  }
}
</script>

<style lang="scss">
:root{
  --main-brown: #734338;
  --main-white: #FCFAF2;
  --main-black: #554236;
  --section-brown: #D7C4BB;
}
body{
  margin: 0;
}
.container{
  max-width: 1200px;
  margin: 0 auto;
}
/*header*/
header{
  border-bottom: 10px solid var(--main-brown);
  padding: 0 20px;
  position: sticky;
  top: 0;
  background-color: white;
  padding-top: 10px;
  z-index: 2;
  .header-content{
    display: flex;
    justify-content: space-between;
    .burger-menu{
      display: none;
      padding-top: 20px;
      .burger-line{
        border: 1px solid var(--main-black);
        width: 30px;
        margin-bottom: 10px;
      }
    }
    .logo{
      width: 210px;
      white-space: nowrap;
      overflow: hidden;
      h1{
        display: inline;
      }
    }
    .pc-menu{
      display: flex;
      align-items: center;
      .nav-link{
        display: flex;
        list-style: none;
        padding-left: 0;
        margin: 0;
        background-color: white;
        span{
          font-family: 'Satisfy', cursive;
        }
        li{
          text-align: center;
          a{
            display: inline-block;
            padding: 10px 13px;
            text-decoration: none;
            color: var(--main-black);
            transition: 0.3s ease-out;
            h3{
              margin: 0;
            }
          }
        }
        li:hover a{
          background-color: var(--main-brown);
          color: var(--main-white);
        }
      }
    }
  }
  .mobile-menu{
    position: absolute;
    background-color: var(--main-brown);
    top: 87px;
    left:0px;
    width: 100%;
    z-index: 2;
    ul{
      list-style: none;
      padding-left: 0;
      padding: 0 30px 30px 30px;
      margin: 0;
      li{
        border-bottom: 1px solid var(--main-white);
        a{
          text-decoration: none;
          .mobile-title{
            color: var(--main-white);
            margin-bottom: 0;
            font-size: 1.5rem;
          }
          span{
            font-family: 'Satisfy', cursive;
          }
        }
      }
    }
  }
}
/*footer*/
footer{
  background-color: var(--main-brown);
  padding: 10px;
  .footer-content{
    display: flex;
    justify-content: space-between;
    .sns{
        display: flex;
        align-items: center;
        ul{
          display: flex;
          justify-content: space-between;
          list-style: none;
          padding-left: 0;
          a{
            color: var(--main-white);
            text-decoration: none;
            margin:0 20px;
          }
        }
      }
    .footer-list{
      display: flex;
      align-items: center;
      ul{
        display: flex;
        justify-content: space-between;
        list-style: none;
        padding-left: 0;
        a{
          color: var(--main-white);
          text-decoration: none;
          margin: 0 20px;
          font-size: 1rem;
          border-bottom: 1px solid var(--main-brown);
        }
        a:hover{
          border-bottom: 1px solid var(--main-white);
        }
      }
    }
  }
  .copy{
    margin: 0;
    text-align: center;
    color: var(--main-white);
  }
}
@media (max-width: 767px) {
  header{
    .header-content{
      .burger-menu{
        display: block;
      }
      .logo{
        margin: 0 auto;
      }
      .pc-menu{
        display: none;
      }
    }
  }
}
@media (max-width: 567px) {
  footer{
    .footer-content{
      .sns{
        margin: 0 auto;
      }
      .footer-list{
        display: none;
      }
    }
  }
}
</style>
