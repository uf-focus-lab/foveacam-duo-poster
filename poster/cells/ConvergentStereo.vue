<script setup lang="ts">
import GridBox from "poster/components/GridBox.vue";
import { Architecture, Results } from "assets/convergent-stereo";

const { accent = "currentColor" } = defineProps<{ accent?: string }>();
</script>

<template>
  <GridBox title="Convergent Stereo" :accent="accent">
    <Architecture />
    <div class="divider"></div>
    <Results />
  </GridBox>
</template>

<style scoped>
.divider {
  border-top: 1mm dotted black;
  margin: 4mm 0;
}
</style>
