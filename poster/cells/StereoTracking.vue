<script setup lang="ts">
import GridBox from "poster/components/GridBox.vue";
import StereoTracking from "assets/stereo-tracking";

const { accent = "currentColor" } = defineProps<{ accent?: string }>();
</script>

<template>
  <GridBox title="StereoTracking" :accent="accent">
    <figure>
      <StereoTracking
        class="svg"
        role="img"
        aria-label="Stereo tracking results"
      />
    </figure>
  </GridBox>
</template>

<style scoped>
figure {
  margin: 0 2mm 3mm 2mm;
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
