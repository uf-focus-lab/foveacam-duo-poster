<script setup lang="ts">
import GridBox from "poster/components/GridBox.vue";
import { Setup, Regression, Rectification } from "assets/calibration";

const { accent = "currentColor" } = defineProps<{ accent?: string }>();
</script>

<template>
  <GridBox title="Calibration" :accent="accent">
    <div class="cell-column">
      <figure class="fig slot-figure">
        <Setup class="svg" role="img" aria-label="Calibration setup" />
      </figure>
      <div class="divider"></div>
      <figure class="fig slot-figure">
        <Regression
          class="svg"
          role="img"
          aria-label="Reprojection error regression"
        />
      </figure>
      <div class="divider"></div>
      <figure class="fig slot-figure">
        <Rectification
          class="svg"
          role="img"
          aria-label="Rectification results"
        />
      </figure>
    </div>
  </GridBox>
</template>

<style scoped>
.cell-column {
  display: flex;
  flex-direction: column;
  gap: 6mm;
  min-height: 0;
  justify-content: space-between;
  height: 100%;
  width: 100%;
}
.divider {
  border-top: 1mm dotted black;
  margin: 5mm 0;
}
.slot-figure {
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
