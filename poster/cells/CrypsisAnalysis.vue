<script setup lang="ts">
import GridBox from "poster/components/GridBox.vue";
import Crypsis from "assets/crypsis";

const { accent = "currentColor" } = defineProps<{ accent?: string }>();
</script>

<template>
  <GridBox title="Crypsis Analysis" :accent="accent">
    <figure>
      <Crypsis class="svg" role="img" aria-label="Crypsis analysis results" />
    </figure>
  </GridBox>
</template>

<style scoped>
figure {
  margin: 8mm 4mm 4mm 4mm;
  min-height: 0;
  display: flex;
  flex-direction: column;
  gap: 0.2em;
}
figure img,
figure .svg {
  width: 100%;
  flex: 1;
  min-height: 0;
  object-fit: contain;
}
figure :deep(svg) {
  width: 100%;
  height: 100%;
  display: block;
  object-fit: contain;
}
</style>
