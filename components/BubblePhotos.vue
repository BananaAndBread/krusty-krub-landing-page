<template>
  <div class="container">
    <div class="image1 image">
    <RoundedImage image-src="krusty-krab-inside.jpg" border-radius="50%"></RoundedImage>
    </div>
    <div class="image2 image" >
      <RoundedImage image-src="krusty-krab-outside.jpg" border-radius="50%"></RoundedImage>
    </div>
    <div class="image3 image">
      <RoundedImage image-src="spongebob.jpeg" border-radius="50%"></RoundedImage>
    </div>
  </div>
</template>

<script>
import RoundedImage from './RoundedImage'
export default {
  name: 'BubblePhotos',
  components: { RoundedImage }
}
</script>

<style scoped>
  .image{
    border: 4px lightskyblue solid;
    border-radius: 50%;
  }
  .image1{
    grid-column: 5/span 3;
    grid-row: 7/span 3;
  }
  .image2{
    grid-column: 1/span 4;
    grid-row: 4/span 4;
    z-index: 1;
  }
  .image3{
    grid-column: 4/span 6;
    grid-row: 1/span 6;
  }
  .container{
    position: relative;
    display: grid;
    grid-template-columns: repeat(10, 1fr);
    grid-template-rows: repeat(10, auto);
  }
  /*.image{*/
  /*  position: absolute;*/
  /*  width: 10%;*/
  /*}*/
  /*.image1{*/
  /*}*/
  /*.image2{*/
  /*}*/
  /*.image3{*/

  /*}*/
  /*.container{*/
  /*  position: relative;*/
  /*}*/
  /*.container div::before {*/
  /*  content: "";*/
  /*  padding-bottom: 100%;*/
  /*  display: inline-block;*/
  /*  vertical-align: top;*/
  /*}*/

</style>
