<template>
  <div>
    <MainPicture />
    <!--    <CustomText />-->
    <MenuElement />
    <!--    <MainDishes/>-->
    <!--    <Map/>-->
  </div>
</template>
<script>
import MenuElement from '../components/Menu/MenuElement'
import MainPicture from '~/components/MainPicture'
import Map from '~/components/Map'
import CustomText from '~/components/CustomText'
import MainDishes from '~/components/SpecialOffers'
export default {
  components: {
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
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
