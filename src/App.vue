<template>
  <header>
    <div class="header-content">
        <div class="logo">
          <router-link to="/">
            <img src="./assets/logo.png" alt="logo">
            <h1>Cage_Cafe</h1>
          </router-link>
        </div>
        <nav>
          <ul class="nav-link">
            <li>
              <router-link to="/">首頁</router-link>
            </li>
            <li>
              <router-link to="/about">最新消息</router-link>
            </li>
            <li>
              <router-link to="/about">關於我們</router-link>
            </li>
            <li>
              <router-link to="/about">美味餐點</router-link>
            </li>
            <li>
              <router-link to="/about">門市資訊</router-link>
            </li>
          </ul>
        </nav>
      </div>
  </header>
  <main>
    <div class="container">
      <router-view/>
    </div>
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
              <router-link to="/about">企業社會責任</router-link>
            </li>
            <li>
              <router-link to="/about">網站地圖</router-link>
            </li>
            <li>
              <router-link to="/about">徵才情報</router-link>
            </li>
            <li>
              <router-link to="/about">聯絡我們</router-link>
            </li>
          </ul>
        </div>
      </div>
      <p class="copy"><small>copyright&copy; 2022 CageCafe, All Rights Reserved.</small></p>
    </div>
  </footer>
</template>

<style lang="scss">
:root{
  --main-brown: #734338;
  --main-white: #FCFAF2;
  --main-black: #554236;
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
    .logo{
      width: 210px;
      white-space: nowrap;
      overflow: hidden;
      h1{
        display: inline;
      }
    }
  }
  nav{
    display: flex;
    align-items: center;
    .nav-link{
      display: flex;
      list-style: none;
      padding-left: 0;
      margin: 0;
      a{
        text-decoration: none;
        font-size: 1.2rem;
        font-weight: bold;
        padding: 10px 25px;
        color: var(--main-black);
      }
      a:hover{
        background-color: var(--main-brown);
        color: var(--main-white);
      }
    }
  }
}
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
            margin-left: 20px;
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
          margin-right: 20px;
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
    margin-bottom: 0;
    text-align: center;
    color: var(--main-white);
  }
}
</style>
