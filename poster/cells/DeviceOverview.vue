<script setup lang="ts">
import Device from "assets/device";
</script>

<template>
  <div class="device-cell">
    <figure class="fig slot-figure">
      <Device class="svg" role="img" aria-label="Device overview" />
    </figure>
  </div>
</template>

<style scoped>
.device-cell {
  min-width: 0;
  min-height: 0;
  display: flex;
  padding: 16mm 16mm 0 16mm;
}
.slot-figure {
  flex: 1;
  min-height: 0;
}
.fig {
  margin: 0;
  min-height: 0;
  display: flex;
  flex-direction: column;
  gap: 0.2em;
}
.fig img,
.fig .svg {
  width: 100%;
  flex: 1;
  min-height: 0;
  object-fit: contain;
}
.fig :deep(svg) {
  width: 100%;
  height: 100%;
  display: block;
  object-fit: contain;
}
</style>
