<template>
  <div :class="{center: true, [size]: true}">
    <div class="text">
      <h1>Claw your way to the Krusty Krab!</h1>
      <hr>
      <p>
        The Krusty Krab is known for being established to sell the Krabby Patty burger.
        The Krabby Patty was invented by King Krabs, an ancestor of restaurant-founder Eugene H.
        Krabs  The recipe was kept secret for over 800 years, but now you can taste Krabby Patty
        EXCLUSIVELY in Krusty Krab!
      </p>
      <p>
        Today, the Krusty Krab uses the latest achievements in fast food technology. Modernization is the heart of the Krusty Krab.
        Some examples of this technology are as follows:
      </p>
      <ul>
        <li>Spatula: An advanced patty-control mechanism.</li>
        <li>Cash register: An automated money-handling system.</li>
        <li>Ice Cubes: Imported high-quality temperature devices.</li>
        <li>Straws: Prototype liquid transfer machines.</li>
        <li>Ketchup packets: State of the art condiment dispersal units.</li>
      </ul>
    </div>
    <BubblePhotos class="bubble-photos" />
  </div>
</template>

<script>
import BubblePhotos from './BubblePhotos'
export default {
  components: {
    BubblePhotos
  },
  props: {
    size: {
      default: '',
      type: String
    }
  }
}

</script>

<style scoped>
  .center.lg{
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
  .center.lg .bubble-photos{
    width: 100%;
    align-self: start;
  }
  .center.sm .bubble-photos{
    width: 100%;
  }
  .center.exsm .bubble-photos{
    width: 100%;
  }
  .bubble-photos{
    margin-top: 5em;
    width: 75%;
  }
  h1{
    margin-top: 1em;
    margin-bottom: 0.5em;
    font-family: "Poppins", sans-serif;
  }
  p{
    margin-top: 32px;
    font-family: "Poppins", sans-serif;
  }
  ul{
    margin-top: 1em;
    font-family: "Poppins", sans-serif;
    margin-left: 2em;
  }
  .text{
    padding-left: 2em;
    padding-right: 2em;
  }
  hr{
    width: 25%;
    border-top: rgb(219, 154, 100) 2px solid;
  }

</style>
