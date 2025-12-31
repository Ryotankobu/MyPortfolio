<script setup>
    import { computed } from 'vue'
    const props = defineProps ({
        title: String,
        currentStatus: String
    })

    const buttonStatus = computed(() => {
        if (props.title === 'Programming') {
            return 'programming'
        } 
        if (props.title === 'BA') {
            return 'ba'
        }
        else {
            return 'other'
        }
    })

    const isButtonActive = computed(() => {
        return props.currentStatus === buttonStatus.value
    })



</script>

<template>
    <button class="w-100 skill-button" :class="{ active: isButtonActive}"> <span>{{ title }}</span></button>
</template>

<style scoped>
button {
 outline: none;
 cursor: pointer;
 border: none;
 padding: 0.9rem 2rem;
 margin: 0;
 font-family: inherit;
 font-size: inherit;
 position: relative;
 display: inline-block;
 letter-spacing: 0.05rem;
 font-weight: 700;
 font-size: 17px;
 /* border-radius: 500px; */
 border-radius: 50% 10% 50% 10% / 10% 50% 10% 50%;
 overflow: hidden;
 background: var( --skill-button-background-before);
 color: ghostwhite;
}
button span {
 position: relative;
 z-index: 10;
 transition: color 0.4s;
}

button:hover span {
 color: ghostwhite;
}

button::before,
button::after {
 position: absolute;
 top: 0;
 left: 0;
 width: 100%;
 height: 100%;
 z-index: 0;
}

button::before {
 content: "";
 background: var( --skill-button-background-after);
 width: 120%;
 left: -10%;
 transform: skew(30deg);
 transition: transform 0.4s cubic-bezier(0.3, 1, 0.8, 1);
}

button:hover::before {
 transform: translate3d(100%, 0, 0);
}
.skill-button.active {
  text-decoration: underline;
  transform: rotate(7deg);
  color: var(--button-background);
}
.skill-button {
font-family: "Press Start 2P", system-ui;
  font-weight: 200;
  font-style: normal;
  font-size: 0.8rem;
}

@media (max-width: 992px) {
  .skill-button.active {
    transform: rotate(0deg);
  }
  .skill-button {
    margin-top: 5px;
  }
}



</style>
