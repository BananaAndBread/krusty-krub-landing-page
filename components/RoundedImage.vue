<template>
  <div :style="{width: width}">
    <div class="image-container">
      <div class="dummy" />
      <img :src="require('@/static/' + imageSrc)" class="image" v-bind:style="{'border-radius': borderRadius}">
    </div>
  </div>
</template>
<script>
export default {
  name: 'RoundedImage',
  props: {
    width: String,
    imageSrc: {
      type: String,
      default: 'krusty-krab-inside.png'
    },
    borderRadius: {
      type: String,
      default: '5%'
    }
  }
}
</script>

<style scoped>
  .dummy{
    margin-top: 100%;
  }
  .image {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    object-fit: cover;
    box-sizing: border-box;
    width: 100%;
    height: 100%;
    border-radius: 5%;
  }
  .image-container {
    position: relative;
    display: flex;
    justify-self: stretch;
    align-self: stretch;
    width: 100%;
  }
</style>
