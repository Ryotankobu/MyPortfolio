<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'
import icon1 from '@/assets/images/bellsprout.png'
import icon2 from '@/assets/images/bellsprout.png'
import icon3 from '@/assets/images/bellsprout.png'

 const props = defineProps({
        title: String,
        description: String,
        leftIcons: {
          type: Array,
          default: () => [],
        },
        rightIcons: {
          type: Array,
          default: () => [,]
        }
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
  <div class="row align-items-stretch">
    <!-- header left area -->
    <div class="col-2 header-left-area icon-area h-100">
      <img 
      v-for="(icon, i) in props.leftIcons"
      :key="'L'+i"
      :src="icon.src"
      class="side-icon"
      :class="{'side-icon--visible': isVisible}"
      :style="{
        left: icon.left,
        top: icon.top,
        animationDelay: `${0.5 + i * 0.5}s`,
        '--rotate': icon.transform
      }">
    </div>
    <!-- header middle area -->
    <div 
    ref="headerRef"
    class="section-header text-center col-8 pt-4 pb-4 mb-4"
    :class="{'section-header--visible': isVisible}">
        <h1 class="section-header-title pb-3 display-2 fw-bold">{{ props.title }}</h1>
        <p class="section-header-description">{{ props.description }}</p>
    </div>
    <!-- header left area -->
    <div class="col-2 header-right-area icon-area h-100">
      <img 
      v-for="(icon, i) in props.rightIcons"
      :key="'L'+i"
      :src="icon.src"
      class="side-icon"
      :class="{'side-icon--visible': isVisible}"
      :style="{
        left: icon.left,
        top: icon.top,
        animationDelay: `${0.7 + i * 0.55}s`,
         '--rotate': icon.transform
      }">
    </div>

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

/* side icon areas */
.icon-area {
  position: relative;
  height: 100%;
  min-height: 230px;
}
.side-icon {
  position: absolute;
  width: 130px;
  height: 130px;
  object-fit: contain;
  opacity: 0;
  transform: scale(0.8) var(--rotate);
}
.side-icon--visible {
  animation: iconPop 0.2s ease-out forwards;
}
@keyframes iconPop {
  0% {
    opacity: 0;
    transform: translateY(10px) scale(0.55) var(--rotate);
  }
  100% {
    opacity: 1;
    transform: translateY(0) scale(1) var(--rotate);
  }
}
</style>