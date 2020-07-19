<template>
  <div class="center">
    <div class="grid">
      <div class="dish">
        <div class="dummy"></div>
        <img src="~/static/menu/krusty-krab-pizza.png" class="image__dish">
      </div>
      <div class="text">
        X
      </div>
      <div class="dish">
        <div class="dummy"></div>
        <img src="~/static/menu/krusty-krab-pizza.png" class="image__dish">
      </div>
      <div class="text">
        X
      </div>
      <div class="dish">
        <div class="dummy"></div>
        <img src="~/static/menu/krusty-krab-pizza.png" class="image__dish">
      </div>
      <div class="text">
        X
      </div>
    </div>
  </div>
</template>

<script>
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
  }

  .dummy{
    margin-top: 100%;
  }
  .image__dish{
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    object-fit: cover;
    box-sizing: border-box;
    width: 100%;
    height: 100%;
  }
</style>
