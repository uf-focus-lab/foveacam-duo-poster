<script setup lang="ts">
import QRCode from "poster/components/QRCode.vue";
</script>

<template>
  <div class="links-row">
    <a href="https://z-yx.cc/SGzn" target="_blank" rel="noopener noreferrer">
      <QRCode url="z-yx.cc/SGzn" class="qr-code" />
      <h5>
        <div class="link-label">Project<br />Website</div>
      </h5>
    </a>
    <a href="https://z-yx.cc/Awz4" target="_blank" rel="noopener noreferrer">
      <QRCode url="z-yx.cc/Awz4" class="qr-code" />
      <h5>
        <div class="link-label">PDF<br />Paper</div>
      </h5>
    </a>
    <a href="https://z-yx.cc/wdAB" target="_blank" rel="noopener noreferrer">
      <QRCode url="z-yx.cc/wdAB" class="qr-code" />
      <h5>
        <div class="link-label">Digital<br />Poster</div>
      </h5>
    </a>
    <a href="https://z-yx.cc/xQ2A" target="_blank" rel="noopener noreferrer">
      <QRCode url="z-yx.cc/xQ2A" class="qr-code" />
      <h5>
        <div class="link-label">Video<br />Intro</div>
      </h5>
    </a>
  </div>
</template>

<style scoped>
.links-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  min-width: 0;
  border-radius: 12mm;
  background: #efefef;
  padding: 10mm 16mm;
}
.links-row a {
  display: flex;
  align-items: center;
  gap: 6mm;
  min-width: 0;
  color: inherit;
  text-decoration: none;
  user-select: none;
}
.qr-code {
  width: 28mm;
  height: 28mm;
  color: var(--text-1);
  flex: 0 0 auto;
}
.links-row a h5 {
  min-width: 0;
  margin: 0;
}
.link-label {
  font-size: 0.8em;
  font-weight: 700;
  letter-spacing: -0.02em;
}
.link-url {
  font-size: 0.55em;
  color: var(--text-2);
  word-break: break-all;
}
</style>
