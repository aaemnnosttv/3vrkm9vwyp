<template>
<div class="Tile"
  :style="{
    backgroundImage: `url(${imgUrl})`
  }"
>
  <span class="Tile__content" :class="{ 'has-desc': desc }">
    <span class="Tile__content_inner">
      <span class="Tile__title" v-text="title"></span>
      <span class="Tile__desc" v-text="desc" v-if="desc"></span>
    </span>
  </span>
  <span class="Tile__overlay"></span>
</div>
</template>

<script>
  export default {
    props: ['title', 'desc', 'image', 'href', 'imgUrl'],
  }
</script>

<style>
.Tile {
  display: flex;
  overflow: hidden;
  height: 100%;
  background-size: cover;
  background-position: center;

  --text-color: var(--gray);
  --bg-color: var(--green);
  --overlay-color: var(--text-color);
}
.Tile.alt {
  --text-color: var(--green);
  --bg-color: var(--gray);
}
.Tile__content {
  position: absolute;
  bottom: 0;
  width: 100%;
  text-align: left;
  display: flex;
  flex-direction: column;
  color: var(--text-color);
}
.Tile__content_inner {
  margin-right: auto;
  padding: .25rem 3rem;
  background-color: var(--bg-color);
}
.Tile__title {
  text-transform: uppercase;
  text-align: left;
  min-width: 30%;
  font-size: 1.25rem;
  font-weight: bold;
}
.Tile__desc {
  display: block;
}
.Tile__overlay {
  display: flex;
  width: 100%;
  height: 100%;
  opacity: 0;
  background-color: var(--overlay-color);
}

@media screen and (max-width: 767px) {
  .Tile__content {
    background-color: var(--bg-color);
    padding: 1.5rem 0;
  }
  .Tile__overlay {
    display: none;
  }
}

@media screen and (min-width: 768px) {
  .Tile:hover .Tile__overlay {
    opacity: .5;
  }
  .Tile__content {
    position: absolute;
    z-index: 10;
    left: 0;
    height: 40%;
  }
  .Tile__desc {
    display: none;
  }
  .Tile:hover .Tile__content.has-desc,
  .Tile__content.has-desc:hover {
    background: var(--bg-color);
  }
  .Tile:hover .has-desc .Tile__desc,
  .Tile__content.has-desc:hover .Tile__desc {
    display: block;
  }
}
</style>