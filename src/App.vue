<template>
  <header>
    <div class="container">
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
              <router-link to="/about" name="about">關於我們</router-link>
            </li>
            <li>
              <router-link to="/about">最新消息</router-link>
            </li>
            <li>
              <router-link to="/about">美味餐點</router-link>
            </li>
            <li>
              <router-link to="/about">分店情報</router-link>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
  <main>
    <div class="container">
      <router-view/>
    </div>
  </main>
  <footer>
    <div class="container">footer</div>
  </footer>
</template>

<style lang="scss">
body{
  margin: 0;
}
.container{
  width: 1200px;
  margin: 0 auto;
}
/*header*/
header{
  border-bottom: 10px solid brown;
  .header-content{
    display: flex;
    justify-content: space-between;
    .logo{
      width: 300px;
      white-space: nowrap;
      overflow: hidden;
      h1{
        display: inline;
      }
    }
  }
  nav{
    display: flex;
    align-items: flex-end;
    .nav-link{
      display: flex;
      list-style: none;
      padding-left: 0;
      margin: 0;
      a{
        text-decoration: none;
        font-size: 1.5rem;
      }
    }
  }
}

</style>
