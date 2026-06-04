<script setup lang="ts">
import Poster from "framework/src/Poster.vue";
import Header from "poster/cells/Header.vue";
import Abstract from "poster/cells/Abstract.vue";
import DeviceOverview from "poster/cells/DeviceOverview.vue";
import TechnicalDetails from "poster/cells/TechnicalDetails.vue";
import Calibration from "poster/cells/Calibration.vue";
import TargetLocalization from "poster/cells/TargetLocalization.vue";
import StereoTracking from "poster/cells/StereoTracking.vue";
import CrypsisAnalysis from "poster/cells/CrypsisAnalysis.vue";
import ConvergentStereo from "poster/cells/ConvergentStereo.vue";
import Links from "poster/cells/Links.vue";
</script>

<template>
  <Poster>
    <header>
      <Header />
    </header>
    <main class="poster-body">
      <div class="top-row">
        <Abstract />
        <DeviceOverview />
        <TechnicalDetails accent="hsl(0, 0%, 32%)" />
      </div>

      <Calibration class="grid-col-1" accent="hsl(220, 60%, 36%)" />

      <div class="grid-col-2-3">
        <TargetLocalization class="target-cell" accent="hsl(220, 60%, 36%)" />
        <StereoTracking class="stereo-cell" accent="hsl(160, 60%, 32%)" />
        <CrypsisAnalysis class="crypsis-cell" accent="hsl(160, 60%, 32%)" />
      </div>

      <div class="grid-col-4-stack">
        <ConvergentStereo accent="hsl(300, 60%, 32%)" />
        <Links />
      </div>
    </main>
  </Poster>
</template>

<style scoped>
header {
  height: 100mm;
  padding: 16mm;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  background: linear-gradient(
    110deg,
    hsl(214 88% 12%) 0%,
    hsl(209 70% 27%) 100%
  );
  color: white;
}
main {
  height: 100%;
  padding: 16mm;
  display: grid;
  grid-template-columns: 2fr 3fr 2fr 4fr;
  grid-template-rows: 5fr 9fr;
  gap: 12mm;
  flex: 1;
  min-width: 0;
  min-height: 0;
}
.top-row {
  grid-column: 1 / -1;
  grid-row: 1;
  display: grid;
  grid-template-columns: 3fr 5fr 6fr;
  gap: 12mm;
  min-width: 0;
  min-height: 0;
}
.grid-col-1 {
  grid-column: 1;
  grid-row: 2;
}
.grid-col-2-3 {
  grid-column: 2 / 4;
  grid-row: 2;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 5fr 4fr;
  gap: 12mm;
  min-width: 0;
  min-height: 0;
}
.target-cell {
  grid-column: 1 / -1;
  grid-row: 1;
}
.stereo-cell {
  grid-column: 1;
  grid-row: 2;
}
.crypsis-cell {
  grid-column: 2;
  grid-row: 2;
}
.grid-col-4-stack {
  grid-column: 4;
  grid-row: 2;
  display: grid;
  grid-template-rows: 1fr auto;
  gap: 12mm;
  min-width: 0;
  min-height: 0;
}
</style>
