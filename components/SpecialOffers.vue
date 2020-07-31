<template>
  <div class="center">
    <div class="grid">
      <RoundedImage :imageSrc="'specialOffers/' + specialOffers[0]['image']" border-radius="0">
      </RoundedImage>
      <div class="arrow-up">
      </div>
      <div class="text">
        {{ specialOffers[2]["description"] }}
      </div>
      <RoundedImage :imageSrc="'specialOffers/' + specialOffers[1]['image']" border-radius="0"></RoundedImage>
      <div class="text">
        {{ specialOffers[0]["description"]}}
      </div>
      <RoundedImage :imageSrc="'specialOffers/' + specialOffers[2]['image']" border-radius="0"></RoundedImage>
      <div class="text">
        {{ specialOffers[1]["description"]}}
      </div>
    </div>
  </div>
</template>

<script>
import RoundedImage from './RoundedImage'
import specialOffers from '~/assets/specialOffers.js'
export default {
  components:
    { RoundedImage },
  mounted () {
    console.log(specialOffers)
  },
  data () {
    return {
      specialOffers
    }
  }
}

</script>

<style scoped>
  .center {
    display: flex;
    justify-content: center;
  }
  .grid {
    width: 85%;
    display: grid;
    grid-template-rows: 1fr 1fr;
    grid-template-columns: 1fr 1fr 1fr;
  }

  .dish {
    position: relative;
    display: flex;
    background-color: gray;
    /*box-sizing: border-box;*/
    justify-self: stretch;
    align-self: stretch;
  }
  .text {
    display: flex;
    margin: 10px;
    font-family: Poppins, sans-serif;
  }
  .arrow-up {
    width: 0;
    border-left: 5px solid transparent;
    border-right: 5px solid transparent;
    border-bottom: 5px solid black;
    position: absolute;
  }

  .arrow-down {
    width: 0;
    height: 0;
    border-left: 20px solid transparent;
    border-right: 20px solid transparent;

    border-top: 20px solid #f00;
  }
</style>
