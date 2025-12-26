<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'
import SectionHeader from "./common/SectionHeader.vue";
import sampleImage from "@/assets/images/bellsprout.png";
import myAboutImage from "@/assets/images/myAboutImage.png";
import SkillButton from "./common/SkillButton.vue";
import SkillboxAreaProgramming from './common/SkillboxAreaProgramming.vue';
import SkillboxAreaBa from './common/SkillboxAreaBa.vue';
import SkillboxAreaOthers from './common/SkillboxAreaOthers.vue';
// icons for SectionHeader
import icon1 from '@/assets/images/sectionHeaderIcons/ryotaLogo.png'
import icon2 from '@/assets/images/sectionHeaderIcons/ryotaLogo.png'
import icon3 from '@/assets/images/sectionHeaderIcons/ryotaLogo.png'

const leftColRef = ref(null)
const rightColRef = ref(null)

const leftVisible = ref(false)
const rightVisible = ref(false)

let observer = null

const selectedSkillType = ref('programming')
const handleSkillCategory = (chosenCategory) => {
  selectedSkillType.value = chosenCategory
}


onMounted(() => {
  observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (!entry.isIntersecting) return

        if (entry.target === leftColRef.value) {
          leftVisible.value = true
          observer.unobserve(entry.target) // only animate once
        }
        if (entry.target === rightColRef.value) {
          rightVisible.value = true
          observer.unobserve(entry.target)
        }
      })
    },
    {
      threshold: 0.3, // trigger when ~30% of the column is visible
    }
  )

  if (leftColRef.value) observer.observe(leftColRef.value)
  if (rightColRef.value) observer.observe(rightColRef.value)
})

onBeforeUnmount(() => {
  if (!observer) return
  if (leftColRef.value) observer.unobserve(leftColRef.value)
  if (rightColRef.value) observer.unobserve(rightColRef.value)
})

const leftIcons = [
  { src: icon1, left: '15%', top: '%', transform: 'rotate(-20deg)' },
  { src: icon2, left: '45%', top: '35%', transform: 'rotate(20deg)' },
  { src: icon3, left: '%0', top: '40%', transform: 'rotate(10deg)' },
]

const rightIcons = [
  { src: icon1, left: '60%', top: '40%', transform: 'rotate(30deg)' },
  { src: icon2, left: '10%', top: '20%', transform: 'rotate(-20deg)' },
  { src: icon3, left: '45%', top: '0%', transform: 'rotate(10deg)' },
]
</script>

<template>
  <div id="about" class="section-anchor"></div>
  <div class="about-container d-flex flex-column py-5 px-5 mb-5">
    <SectionHeader
      title="Know More About Me"
      description="As a mature‑age developer, I bring discipline, clarity, and a practical mindset to my work. My skills span front‑end development, business analysis, and communication — shaped by both technical training and diverse professional experience."
    :left-icons="leftIcons"
    :right-icons="rightIcons"
      />
    <div class="about-section-main container-fluid flex-grow-1">
      <div class="row h-100">
        <div 
        ref="leftColRef"
        class="col-4 p-0 pe-2 about-col about-col--left"
        :class="{ 'about-col--visible': leftVisible }">
          <div
            class="card left-card p-4 h-100 d-flex flex-column justify-content-between border border-3 border-success" style="background-color: var(--left-about-card);"
          >
            <div class="border rounded  border border-2 border-dark d-flex align-items-center justify-content-center py-2 mb-4">
              <h4 class="m-0 charactor-status-text">HP  100/100</h4>
            </div>
            <img
              :src="myAboutImage"
              class="card-img-top w-75 hero-image mx-auto d-block border border-4 border-dark"
              alt="..."
            />
            <div class="border rounded border border-2 border-dark d-flex align-items-center justify-content-center py-2 mt-4">
              <h4 class="m-0 charactor-status-text">LOYALITY  100/100</h4>
            </div>
          </div>
        </div>

        <div 
        class="col-8 h-100 p-0 ps-2 about-col about-col--right"
        ref="rightColRef"
        :class="{ 'about-col--visible': rightVisible }">
          <div class="card h-100 p-4 d-flex flex-column justify-content-between border border-9 border-warning" style="background-color: var(--main-background);">
            <div class="skill-button-area d-flex flex-row justify-content-around">
                <SkillButton title="Programming" :currentStatus=selectedSkillType class="mx-2" @click="handleSkillCategory('programming')"/>
                <SkillButton title="BA" :currentStatus=selectedSkillType class="mx-2" @click="handleSkillCategory('ba')"/>
                <SkillButton title="Others" :currentStatus=selectedSkillType class="mx-2" @click="handleSkillCategory('other')"/>
            </div>

            <SkillboxAreaProgramming v-if="selectedSkillType === 'programming'" />
            <SkillboxAreaBa v-else-if="selectedSkillType === 'ba'"/>
            <SkillboxAreaOthers v-else/>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.border-9 {
  border-width: 9px !important;
}
.about-container {
  scroll-margin-top: 80px;
}
.skill-box {
  flex: 1;
  transition: all .3s ease-in-out;
}
.skill-box:hover {
  transform: scale(1.01);
  box-shadow: 5px 5px var(--shadow-color);

}
.card {
  box-shadow: 10px 12px  var(--shadow-color); 
}
.left-card {
  transform: rotate(-2deg);
}
.charactor-status-text {
  font-family: "Luckiest Guy", cursive;
  font-weight: 400;
  font-style: normal;
}

.about-col {
  opacity: 0;
  transform: translateY(20px);
 
}
.skill-level-number-box {
  font-family: "Luckiest Guy", cursive;
  font-weight: 400;
  font-style: normal;
}

/* Left column starts slightly left, right slightly right */
.about-col--left {
  opacity: 0;
  transform: translateX(-40px);
  /* box-shadow: 10px 12px  var(--shadow-color); */
}

.about-col--right {
  opacity: 0;
  transform: translateX(40px);
  /* box-shadow: 10px 12px  var(--shadow-color); */
}

/* When visible, play animation */
.about-col--visible.about-col--left {
  animation: slideInLeft 0.8s ease-out forwards;
}

.about-col--visible.about-col--right {
  animation: slideInRight 0.8s ease-out forwards;
  animation-delay: 0.3s; 
}

@keyframes slideInLeft {
  0% {
    opacity: 0;
    transform: translateX(-40px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideInRight {
  0% {
    opacity: 0;
    transform: translateX(40px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

</style>
