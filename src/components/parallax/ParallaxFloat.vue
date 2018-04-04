<template>
  <div class="ParallaxFloat" :style="{ transform: 'translateZ(' + tz + 'px) scale(' + sx + ')' }">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'ParallaxFloat',
  data: () => ({
    tz: 50,
    sx: 0.5
  }),
  props: {
    offset: {
      default: 0.3,
      type: Number
    }
  },
  created: function() {
    this.tz = 100 - ((1 - this.offset) * 100);
    this.sx = 1 - this.offset
  }
}
</script>

<style scoped>
.ParallaxFloat {
  position: relative;
  pointer-events: none;
  left: 0;
  right: 0;
}

.ParallaxFloat > * {
  pointer-events: auto;
}
</style>
