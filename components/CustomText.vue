<template>
  <div
    data-aos="fade-up"
    data-aos-delay="500"
    data-aos-once="true"
    class="card"
  >
    <h2 class="title">
      The most popular restaurant in Bikini Bottom
    </h2>
    <p class="subtitle">
      Try our best food:
    </p>
  </div>
</template>

<script>
export default {
  components: {},
  data () {
    return {}
  }
}
</script>

<style scoped>
  .card {
    text-align: center;
    padding-top: 5em;
    padding-bottom: 5em;
  }
  .title{
    color: #000;
    font-size: 35px;
    font-family: "Playfair Display";
    line-height: 36px;
    font-weight: 500;
    letter-spacing: 0px;
    word-spacing: 0;
  }
  .subtitle{
    color: rgb(128, 128, 128);;
    font-family: "Playfair Display";
    font-size: 25px;
    margin-top: 1em;
    font-weight: 100;
    letter-spacing: 0px;
    word-spacing: 0;
  }

</style>
