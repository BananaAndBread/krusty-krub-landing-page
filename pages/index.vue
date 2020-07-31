<template>
  <div>
    <MainPicture />
    <About :size="this.$mq" />
    <CustomText class="text">
      <template slot="title">
        Menu
      </template>
      <template slot="subtitle">
        Mmm, delicious
      </template>
    </CustomText>
    <Menu />
    <CustomText class="text">
      <template slot="title">
        Special offers (in progress)
      </template>
      <template slot="subtitle">
        2020
      </template>
    </CustomText>
    <div class="special-offers">
      <SpecialOffers />
    </div>
    <Card>
<!--      <template slot="above">-->
<!--        <CustomText class="text">-->
<!--          <template slot="title">-->
<!--            Reservation-->
<!--          </template>-->
<!--          <template slot="subtitle">-->
<!--          </template>-->
<!--        </CustomText>-->
<!--      </template>-->
      <template slot="inside">
        <ReservationForm id="reservation" />
      </template>
    </Card>
    <Map></Map>
    <div>Icons made by <a href="https://www.flaticon.com/authors/freepik" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div>
  </div>
</template>
<script>
import MenuElement from '../components/Menu/MenuElement'
import Menu from '../components/Menu/Menu'
import ReservationForm from '../components/ReservationForm'
import Card from '../components/Card'
import About from '../components/About'
import MainPicture from '~/components/MainPicture'
import Map from '~/components/Map'
import CustomText from '~/components/CustomText'
import SpecialOffers from '~/components/SpecialOffers'
export default {
  components: {
    About,
    // eslint-disable-next-line vue/no-unused-components
    Menu,
    MainPicture,
    // eslint-disable-next-line vue/no-unused-components
    Map,
    // eslint-disable-next-line vue/no-unused-components
    CustomText,
    // eslint-disable-next-line vue/no-unused-components
    // eslint-disable-next-line vue/no-unused-components
    MenuElement,
    ReservationForm,
    SpecialOffers,
    Card
  }
}
</script>

<style scoped>
  /*@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');*/
  body {
    background-color: rgba(238, 238, 238, 0.94);
  }
  .text{
    margin-top: 72px;
  }
  .special-offers{
    margin-top: 5em;
    width: 70%;
    margin-left: auto;
    margin-right: auto;
    margin-bottom: 5em;
  }
</style>
