<template>
  <div class="abstract-cell">
    <h4>Abstract</h4>
    <p>
      FoveaCam Duo is a passive foveated stereo system with MEMS-steered
      telephoto cameras that deliver dense depth at selected regions. The
      steering introduces angle-dependent distortion beyond fixed-geometry
      calibration, we design a three-stage pipeline that maps mirror voltages to
      pointing and rectifies images via affine regression. We show detection
      range quadratically expands the standoff operating region and simulations
      confirm multi-fovea agents greatly increase coverage over single-fovea
      setups. Experiments show accurate localization where wide angle stereo
      fails; we trained a custom stereo depth model to validate the disparity
      signal produced by FoveaCam Duo.
    </p>
  </div>
</template>

<style scoped>
.abstract-cell {
  display: flex;
  flex-direction: column;
  gap: 4mm;
  padding: 2mm 0 0 0;
  min-width: 0;
  min-height: 0;
  overflow: visible;
}
.abstract-cell h4 {
  font-size: 1em;
  margin: 0;
}
.abstract-cell p {
  margin: 0;
  font-size: 0.72em;
  line-height: 1.2;
  color: var(--text-1);
  margin-right: -8mm;
}
</style>
