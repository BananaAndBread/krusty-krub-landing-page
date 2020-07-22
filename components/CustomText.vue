<template>
  <div
    data-aos="fade-up"
    data-aos-delay="500"
    data-aos-once="true"
    class="card"
  >
    <h2 class="title">
      <slot name="title"/>
    </h2>
    <p class="subtitle">
      <slot name="subtitle"/>
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
  }
  .title{
    color: #000;
    font-size: 35px;
    line-height: 36px;
    font-weight: 500;
    letter-spacing: 0px;
    word-spacing: 0;
  }
  .subtitle{
    color: rgb(128, 128, 128);;
    margin-top: 1em;
    font-weight: 100;
    letter-spacing: 0px;
    word-spacing: 0;
  }
  div{
    font-family: "Poppins", sans-serif
  }

</style>
