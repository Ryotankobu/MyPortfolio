<script setup>
defineProps({
  text: { type: String, required: true },
  duration: { type: Number, default: 15 },
});
</script>

<template>
  <div class="marquee-wrapper bg-success">
    <div class="marquee-track" :style="{ animationDuration: `${duration}s` }">
      <span class="marquee-text fw-bold display-4 py-4">{{ text }}</span>
      <span class="marquee-text fw-bold display-4 py-4">{{ text }}</span>
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
}
.marquee-text {
  padding-right: 2rem;
  white-space: nowrap;
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
