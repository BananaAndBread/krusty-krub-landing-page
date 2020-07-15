<template>
  <div class="container">
    <div class="image-size-container">
      <RoundedImage width="100px"/>
    </div>
    <div class="text">
      <h3 class="name">
        Title
      </h3>
      <p class="description">
        Description Description Description Description
      </p>
      <p class="price">
        $20
      </p>
    </div>
  </div>
</template>

<script>
import RoundedImage from '../RoundedImage'
export default {
  components: {
    RoundedImage
  }
}
</script>
<style scoped>

  .image-size-container{
    width: 10em;
  }
  .container{
    display: flex;
    flex-wrap: wrap;
    align-content: flex-start;
    justify-content: center;
    text-align: left;
    align-items: center;
    height: 10em;
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
    justify-content: space-between;
    align-content: space-between;
  }
</style>
