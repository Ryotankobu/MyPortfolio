<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'

    defineProps({
        title: String,
        description: String,
    })

const headerRef = ref(null)
const isVisible = ref(false)
let observer = null
onMounted(() => {
    observer = new IntersectionObserver(
        (entries) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    isVisible.value = true
                    observer.unobserve(entry.target)
                }
            })
        },
        {
            threshold: 0.3,
        }
    )
    if (headerRef.value) {
        observer.observe(headerRef.value)
    }
})

onBeforeUnmount(() => {
  if (observer && headerRef.value) {
    observer.unobserve(headerRef.value)
  }
})

</script>

<template>
    <div 
    ref="headerRef"
    class="section-header text-center col-10 offset-1 pt-4 pb-4 mb-4"
    :class="{'section-header--visible': isVisible}">
        <h1 class="section-header-title pb-3 display-2 fw-bold">{{ title }}</h1>
        <p class="section-header-description">{{ description }}</p>
    </div>

</template>

<style scoped>
    .section-header {
  opacity: 0;
  transform: translateY(24px);
}

/* When visible, play float-in animation once */
.section-header--visible {
  animation: floatIn 1s ease-out forwards;
  animation-delay: 0.3s;
}

@keyframes floatIn {
  0% {
    opacity: 0;
    transform: translateY(24px);
  }
  60% {
    opacity: 1;
    transform: translateY(-6px); /* slight overshoot */
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

/* optional: some base styling */
.section-header-title {
  margin-bottom: 0.5rem;
  font-family: "Bungee", sans-serif;
  font-weight: 400;
  font-style: normal;
}

.section-header-description {
  margin: 0;
  line-height: 1.4;
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 1.1em;
}
</style>