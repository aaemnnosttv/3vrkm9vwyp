<template>
  <div id="app">
    <grid>
      <grid-item :full-width="true">
        <tile title="Coolsculpting"
          img-url="https://user-images.githubusercontent.com/1621608/44595755-c4b58000-a7d2-11e8-8a89-c2a6e40896cd.jpg"
          desc="Lorem ipsum about coolscuplting"
          />
      </grid-item>
      <grid-item>
        <tile title="Emsculpt only at Quintessa"
          img-url="https://user-images.githubusercontent.com/1621608/44595760-c54e1680-a7d2-11e8-9754-2095fa6087cb.jpg"
          desc="Lorem ipsum about Emsculpting... whatever THAT is!"
        />
      </grid-item>
      <grid-item>
        <tile title="Botox"
          img-url="https://user-images.githubusercontent.com/1621608/44595756-c4b58000-a7d2-11e8-85f9-3bd6be854a68.jpg"
          desc="Lorem ipsum about getting some mega big lips"
        />
      </grid-item>
      <grid-item>
        Some products
      </grid-item>
      <grid-item>
        <tile title="Shop Products" />
      </grid-item>
      <grid-item>
        <tile title="Blog"
          img-url="https://user-images.githubusercontent.com/1621608/44595757-c4b58000-a7d2-11e8-9dec-cb4fb37b467a.jpg"
        />
      </grid-item>
      <grid-item span-rows=2>
        <tile class="alt"
          title="Meet our Staff"
          img-url="https://user-images.githubusercontent.com/1621608/44595759-c54e1680-a7d2-11e8-9a52-42efb99fe89a.jpg"
          desc="Our staff is the best in the world and doing everything. Really."
        />
      </grid-item>
      <grid-item>
      <tile title="Promos"
          img-url="https://user-images.githubusercontent.com/1621608/44595761-c54e1680-a7d2-11e8-84b0-60f64971f807.jpg"
        />
      </grid-item>
    </grid>
  </div>
</template>

<script>
import Grid from "./components/Grid";
import GridItem from "./components/GridItem";
import Tile from "./components/Tile";

export default {
  name: "App",
  components: {
    Grid,
    GridItem,
    Tile
  }
};
</script>

<style>
:root {
  --green: #75EBDB;
  --gray: #505052;
}
body {
  margin: 0;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  --grid-breakpoint: 767px;
}
</style>
