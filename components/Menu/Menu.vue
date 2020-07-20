<template>
  <div>
    <Tab :tabs="['main', 'desserts', 'drinks']">
      <template slot="tab-head-main">
        <BurgerIcon class="svg-style" />
        <p>Main</p>
      </template>
      <template slot="tab-head-desserts">
        <DessertIcon class="svg-style" />
        <p>Desserts</p>
      </template>
      <template slot="tab-head-drinks">
        <DrinkIcon class="svg-style" />
        <p>Drinks</p>
      </template>

      <template slot="tab-content-desserts">
        <div class="center">
          <div :class="{menu: true, [$mq]: true}">
            <MenuElement :size="$mq" v-for="menuElement in Menu.desserts" :key="menuElement.name" :info="menuElement" class="menu-element" />
          </div>
        </div>
      </template>
      <template slot="tab-content-main">
        <div class="center">
          <div :class="{menu: true, [$mq]: true}">
            <MenuElement :size="$mq" v-for="menuElement in Menu.main" :key="menuElement.name" :info="menuElement" class="menu-element" />
          </div>
        </div>
      </template>
      <template slot="tab-content-drinks">
        <div class="center">
          <div :class="{menu: true, [$mq]: true}">
            <MenuElement v-for="menuElement in Menu.drinks" :key="menuElement.name" :info="menuElement" class="menu-element" />
          </div>
        </div>
      </template>
    </Tab>
  </div>
</template>

<script>
import Tab from '../Tab'
import MenuElement from './MenuElement'
import DessertIcon from '@/assets/svg/dessert.svg'
import DrinkIcon from '@/assets/svg/drink.svg'
import BurgerIcon from '@/assets/svg/burger.svg'
import Menu from '@/assets/menu.js'
export default {
  // eslint-disable-next-line vue/no-unused-components
  components: {
    MenuElement,
    Tab,
    DessertIcon,
    BurgerIcon,
    DrinkIcon
  },
  data () {
    return {
      Menu: {
        type: Object
      }
    }
  },
  mounted () {
    this.Menu = Menu
    console.log(this.$mq)
  }

}
</script>

<style>
  .menu{
    display: grid;
    width: 85%;
    grid-template-columns: 1fr 1fr;
  }
  .menu-element{
    /*margin: 2em;*/
  }
  .menu.exsm{
    grid-template-columns: 1fr;
  }
  .svg-style {
    width: 50px;
    height: auto;
    margin-bottom: 1em;
    margin-top: 1em;
  }
  .center{
    display: flex;
    justify-content: center;
  }
</style>
