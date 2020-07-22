<template>
  <div class="reserve-table-button">
    <button>Reserve table</button>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
    }
  }
}
</script>
<style scoped>
  button {
    background: rgba(15, 17, 164, 0.25);
    border: 2px solid #fff;
    padding-left: 3rem;
    padding-right: 3rem;
    padding-top: 1rem;
    padding-bottom: 1rem;
    text-transform: uppercase;
    letter-spacing: .2em;
    font-size: 14px;
    font-weight: 700;
    color: white;
    font-family: "Open Sans", Arial, sans-serif;
  }
  button:hover{
    background: white;
    color: black;
  }
</style>
