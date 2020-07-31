<template>
  <div class="background">
    <slot name="above"/>
    <div :class="{card: true, [this.$mq]: true}">
      <slot name="inside"/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card'
}
</script>

<style scoped>
  .background{
    background: rgba(118, 220, 231, 0.22);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .card{
    width: 85%;
    height: 85%;
    background: white;
    margin-top: 5em;
    margin-bottom: 5em;
    padding-top: 3em;
    padding-bottom: 3em;
    box-shadow: 0 10px 20px -5px rgba(0, 0, 0, 0.1);
    max-width: 600px;
  }
  .card.sm{
    width: 100%;
  }
  .card.exsm{
    width: 100%;
  }
</style>
