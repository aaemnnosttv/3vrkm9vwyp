<template>
  <div class="GridItem" :style="styles">
  <slot></slot>
  </div>
</template>

<script>
export default {
  props: ['full-width', 'span-rows'],
  computed: {
    styles() {
      const css = {};

      if (this.fullWidth) {
        css.gridColumn = '1 / -1'
      }

      if (this.spanRows > 1) {
        css.gridRowStart = `span ${this.spanRows}`
      }
      

      return css
    }
  }
}
</script>

<style>
.GridItem {
  position: relative;
  overflow: hidden;
  // box-shadow: inset 0 0 17px 2px #0cb1ff;
}
</style>
