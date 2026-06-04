<script setup lang="ts">
import GridBox from "poster/components/GridBox.vue";
import Design from "assets/design.svg";
import CrossSection from "assets/cross-section.svg";

const { accent = "currentColor" } = defineProps<{ accent?: string }>();
</script>

<template>
  <GridBox title="Technical Details" :accent="accent" class="tech-cell">
    <div class="tech-row-1">
      <div class="tech-left">
        <figure class="fig slot-figure">
          <Design
            class="svg tech-design"
            role="img"
            aria-label="Design overview chart"
          />
        </figure>
      </div>
      <div class="tech-right">
        <figure class="fig slot-figure">
          <CrossSection class="svg" role="img" aria-label="Section view" />
        </figure>
      </div>
    </div>
    <div class="tech-specs">
      <div class="spec-item">
        <h5>Wide FoV</h5>
        <p>25.6° × 19.4°</p>
      </div>
      <div class="spec-item">
        <h5>Fovea FoV</h5>
        <p>2.86° × 2.15°</p>
      </div>
      <div class="spec-item">
        <h5>Wide Ang. Res.</h5>
        <p>~55 px/°</p>
      </div>
      <div class="spec-item">
        <h5>Fovea Ang. Res.</h5>
        <p>~502 px/°</p>
      </div>
      <div class="spec-item">
        <h5>Actuation</h5>
        <p>20° × 20°</p>
      </div>
      <div class="spec-item">
        <h5>Extended FoV</h5>
        <p>22.9° × 22.2°</p>
      </div>
    </div>
  </GridBox>
</template>

<style scoped>
.tech-cell {
  min-width: 0;
  min-height: 0;
}
.tech-cell > :deep(.grid-body) {
  display: grid;
  grid-template-rows: 1fr auto;
}
.tech-row-1 {
  flex: 1;
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 16mm;
  min-width: 0;
  min-height: 0;
}
.tech-left,
.tech-right {
  min-width: 0;
  min-height: 0;
}
.tech-row-1 > * {
  max-height: 100%;
}
.tech-design {
  height: 160mm;
  width: auto;
  flex: none;
}
.tech-specs {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 0 6mm;
}
.spec-item {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: flex-start;
  background-color: #eee;
  outline: 0.5mm solid black;
  padding: 4mm;
  border-radius: 6mm;
  margin: 1mm;
}
.spec-item h5,
.spec-item p {
  margin: 0;
  padding: 0;
}
.spec-item h5 {
  font-size: 0.5em;
  font-weight: bolder;
}
.spec-item p {
  font-size: 0.7em;
  font-weight: 600;
  color: var(--accent);
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
