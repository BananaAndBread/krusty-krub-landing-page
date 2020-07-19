<template>
  <div>
    <MainPicture />
    <!--    <CustomText />-->
    <Menu />
    <!--    <MainDishes/>-->
    <!--    <Map/>-->
    <div>Icons made by <a href="https://www.flaticon.com/authors/freepik" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div>
  </div>
</template>
<script>
import MenuElement from '../components/Menu/MenuElement'
import Menu from '../components/Menu/Menu'
import MainPicture from '~/components/MainPicture'
import Map from '~/components/Map'
import CustomText from '~/components/CustomText'
import MainDishes from '~/components/SpecialOffers'
export default {
  components: {
    // eslint-disable-next-line vue/no-unused-components
    Menu,
    MainPicture,
    // eslint-disable-next-line vue/no-unused-components
    Map,
    // eslint-disable-next-line vue/no-unused-components
    CustomText,
    // eslint-disable-next-line vue/no-unused-components
    MainDishes,
    // eslint-disable-next-line vue/no-unused-components
    MenuElement
  }
}
</script>

<style scoped>
  body {
    background-color: rgba(238, 238, 238, 0.94);
  }

</style>
