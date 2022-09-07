<template>
  <section>
      <div class="container">
        <SwiperSectionVue></SwiperSectionVue>
      </div>
  </section>
  <section class="section-brown">
    <div class="container">
      <NewsSectionVue></NewsSectionVue>
    </div>
  </section>
  <section>
    <div class="container">
      <MenuSectiontVue></MenuSectiontVue>
    </div>
  </section>
  <section class="section-brown">
    <div class="container">
      <StoreSectionVue></StoreSectionVue>
    </div>
  </section>
</template>

<script>
// @ is an alias to /src
import SwiperSectionVue from '@/components/Home/SwiperSection.vue'
import NewsSectionVue from '@/components/Home/NewsSection.vue'
import MenuSectiontVue from '@/components/Home/MenuSection.vue'
import StoreSectionVue from '@/components/Home/StoreSection.vue'

export default {
  name: 'HomeView',
  components: {
    SwiperSectionVue,
    NewsSectionVue,
    MenuSectiontVue,
    StoreSectionVue
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
  .section-brown{
    background-color: var(--section-brown);
  }
</style>
