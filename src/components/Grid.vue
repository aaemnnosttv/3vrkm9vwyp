<template>
  <div class="Grid">
    <slot></slot>
  </div>
</template>

<script>
export default {
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.Grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-auto-rows: 325px;
}

@media screen and (max-width: 767px) {
  .Grid {
    grid-template-columns: 1fr;
  }
}

h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
