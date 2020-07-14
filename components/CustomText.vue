<template>
  <div class="card">
  <h2 class="title">The most popular restaurant in Bikini Bottom
  </h2>
   <p class="subtitle"> Try our best food
   </p>
  </div>
</template>

<script>
export default {
  data () {
    return {}
  },
  components: {}
}
</script>

<style scoped>
  .card {
    text-align: center;
    padding-top: 5em;
    margin-bottom: 10px;
  }
  .title{
    color: #000;
    font-size: 30px;
    font-family: "Playfair Display", serif;
  }
  .subtitle{
    color: rgb(128, 128, 128);;
    font-family: "Playfair Display", serif;
    font-size: 20px;;
    margin-top: 1em;
    font-weight: 300;
  }

</style>
