<script setup lang="ts">
import GridBox from "poster/components/GridBox.vue";
import Localization from "assets/localization";

const { accent = "currentColor" } = defineProps<{ accent?: string }>();
</script>

<template>
  <GridBox title="Target Localization" :accent="accent">
    <figure class="fig slot-figure">
      <Localization
        class="svg"
        role="img"
        aria-label="Target localization experiment setup"
      />
    </figure>
  </GridBox>
</template>

<style scoped>
.cell-column {
  display: flex;
  flex-direction: column;
  gap: 6mm;
  min-height: 0;
  flex: 1;
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
