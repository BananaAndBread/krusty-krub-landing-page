<template>
  <div class="image-container">
    <div class="dummy" />
    <img src="~/assets/menu/krusty-krab-pizza.png" class="image">
  </div>
</template>

<script>
export default {
  name: 'RoundedImage'
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
  }
</style>
