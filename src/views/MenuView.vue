<template>
    <h2>Menu</h2>
    <nav>
        <div class="container">
            <ul>
                <li>
                    <a href="">咖啡</a>
                </li>
            </ul>
        </div>
    </nav>
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
            <LightmealSectionVue></LightmealSectionVue>
        </div>
    </section>
    <section id="dessert">
        <div class="container">
            <DessertSectionVue></DessertSectionVue>
        </div>
    </section>
</template>

<script>
import CoffeeSection from '@/components/Menu/CoffeeSection.vue'
import TeaSectionVue from '@/components/Menu/TeaSection.vue'
import LightmealSectionVue from '@/components/Menu/LightmealSection.vue'
import DessertSectionVue from '@/components/Menu/DessertSection.vue'

export default {
  components: {
    CoffeeSection,
    TeaSectionVue,
    LightmealSectionVue,
    DessertSectionVue
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
</style>
