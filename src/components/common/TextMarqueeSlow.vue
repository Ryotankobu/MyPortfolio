<script setup>
defineProps({
  text: { type: String, required: true },
  duration: { type: Number, default: 30 },
});
</script>

<template>
  <div class="marquee-wrapper py-0 my-0">
    <div class="marquee-track" :style="{ animationDuration: `${duration}s` }">
      <span class="marquee-text fw-bold pt-4">{{ text }}</span>
      <span class="marquee-text fw-bold pt-4">{{ text }}</span>
      <span class="marquee-text fw-bold pt-4">{{ text }}</span>
      <span class="marquee-text fw-bold pt-4">{{ text }}</span>
    </div>
  </div>
</template>

<style scoped>
.marquee-wrapper {
  width: 100%;
  overflow: hidden;
  white-space: nowrap;
  position: relative;
}
.marquee-track {
  display: inline-flex;
  white-space: nowrap;
  animation-name: marquee;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
  display: flex;
  align-items: flex-end;
 
}
.marquee-text {
  padding-right: 8rem;
  white-space: nowrap;
  color: var(--experience-section-background);
  line-height: 0.7;
  font-size: 8rem;
  font-family: "Press Start 2P", system-ui;
  font-weight: 400;
  font-style: normal;
}

@keyframes marquee {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translate(-50%);
  }
}
</style>
