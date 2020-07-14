<template>
  <div>
  <div class="wrapper">
    <div class="shadow" />
    <div class="overlay">
      <div class="text">
        Welcome to the Crusty Krabs!
      </div>
      <div class="reserve-table-button">
        <ReserveTable></ReserveTable>
      </div>
    </div>
    <img class="image image__crusty-krabs" src="~/assets/crusty-krab-transparent.png">
    <img class="image image__background" src="~/assets/background.png">
  </div>
  <div style="height: 1000px"></div>
  </div>
</template>

<script>
import ReserveTable from './Buttons/ReserveTable'
export default {
  components: {
    ReserveTable
  }
}
</script>

<style scoped>
  .wrapper{
    position: relative;
    height: 500px;
    overflow: hidden;
    width: 100%;
    display: flex;
    justify-content: center;

  }
  .reserve-table-button{
    z-index: 2;
  }

  .overlay{
    position: absolute;
    border: 1px solid black;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    height: 100%;
    width: 100%;
  }
  .shadow{
    background-color: rgba(138, 141, 150, 0.31);
    position: absolute;
    width: 100%;
    height: 100%;
    z-index: 1;
  }
  .text {
    font-size: 70px;
    z-index: 2;
    font-family: "Playfair Display", serif;
    color: white;
    font-weight: 900;
    margin-bottom: 60px
  }
  .image{
    position: absolute;
    height: 500px;
    width: auto;
  }
  .image__crusty-krabs{
    z-index: 1;
    min-height: 200px;
    height: 100%;

  }
  .image__background{
    z-index: 0;
    height: auto;
    width: 100%;
    min-width: 1000px;
    max-width: 2000px;
  }
</style>
