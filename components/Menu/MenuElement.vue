<template>
  <div class="container">
    <div class="image">
      <RoundedImage :image-src="info.image" width="150px" />
    </div>
    <div class="text">
      <h3 class="name">
        {{ info.name }}
      </h3>
      <p class="description">
        {{ info.description }}
      </p>
      <p class="price">
        ${{ info.price }}
      </p>
    </div>
  </div>
</template>

<script>
import { ResponsiveDirective } from 'vue-responsive-components'
import RoundedImage from '../RoundedImage'
export default {
  components: {
    RoundedImage
  },
  directives: {
    responsive: ResponsiveDirective
  },
  props: {
    info: {
      type: Object,
      default () {
        return {
          name: 'Pizza',
          description: 'Description Description Description Description',
          image: 'krusty-krab-pizza.png',
          price: '3.99'
        }
      }
    },
    size: {
      type: String,
      default: '',
      validator (value) {
        return ['small', 'extraSmall', ''].includes(value)
      }
    }
  },
  mounted () {
  }
}
</script>
<style scoped>
  .image{
    justify-self: end;
  }
  .container{
    align-items: center;
    display: flex;
  }
  .container.small{
    display: flex;
    flex-direction: column;
  }
  .container.small .image{
    align-self: start;
  }
  .name{
    font-size: 24px;
    font-weight: 400;
    font-family: "Poppins", sans-serif;
    text-align: left;
  }
  .description{
    box-sizing:border-box;
    color:rgb(89, 102, 114);
    font-family: "Poppins", sans-serif;
    font-size:16px;
    text-align: left;
    width: 100%
  }
  .price{
    color:rgb(219, 154, 100);
    font-family:Poppins, sans-serif;
    font-size:26px;
    font-style:normal;
    font-weight:400;
    text-align: left;
  }
  .text{
    margin-left: 1em;
    display: flex;
    flex-direction: column;
    align-self: stretch;
    justify-content: space-around;
    justify-self: start;

  }
  .container.small .text{
    margin-left: 0;
  }
  .container.small .name{
    margin-top: 0.25em;
    margin-bottom: 0.25em;
  }
</style>
