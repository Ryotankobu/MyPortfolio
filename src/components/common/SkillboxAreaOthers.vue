<script setup>
import sampleImage from "@/assets/images/bellsprout.png";
import englishIcon from "@/assets/images/englishIcon.png";
import japaneseIcon from "@/assets/images/japaneseIcon.png";
import diyIcon from "@/assets/images/diyIcon.png";
import laptopIcon from "@/assets/images/laptopIcon.png";
import laravelIcon from "@/assets/images/laravelIcon.png";
</script>
<template>
  <div class="d-flex flex-column h-100 mt-3">
    <!-- EnglishSkill -->
    <div class="border border-3 border-dark rounded mt-2 skill-box">
      <div class="row py-1 px-3 h-100">
        <div
          class="col-4 col-md-2 col-xl-2 icon-box d-flex align-items-center justify-content-center order-xl-1"
        >
          <div class="p-4 bg-white text-center rounded">
            <img :src="englishIcon" class="card-img-top w-100" alt="..." />
          </div>
        </div>
        <div
          class="col-12 col-xl-8 p-xl-10 p-2 skill-details-box d-flex flex-column order-3 order-xl-2"
        >
          <h4 class="skill-box-title">English</h4>
          <p class="tight-text">
            My English level is fluent for professional work, supported by an
            IELTS score of 7.5 and a Cambridge First Certificate in English
          </p>
        </div>
        <div
          class="col-8 col-md-10 col-xl-2 p-xl-0 p-2 skill-level-box d-flex flex-column justify-content-around py-xl-3 order-xl-2"
        >
          <div class="skill-level-number-box border rounded text-center">
            80 / 100
          </div>
          <div class="progress">
            <div
              class="progress-bar bg-success"
              role="progressbar"
              style="width: 80%"
              aria-valuenow="25"
              aria-valuemin="0"
              aria-valuemax="100"
            ></div>
          </div>
        </div>
      </div>
    </div>

    <!-- Japanese Skill -->
    <div class="border border-3 border-dark rounded mt-2 skill-box">
      <div class="row py-1 px-3 h-100">
        <div
          class="col-4 col-md-2 col-xl-2 icon-box d-flex align-items-center justify-content-center order-xl-1"
        >
          <div class="p-4 bg-white text-center rounded">
            <img :src="japaneseIcon" class="card-img-top w-100" alt="..." />
          </div>
        </div>
        <div
          class="col-12 col-xl-8 p-xl-10 p-2 skill-details-box d-flex flex-column order-3 order-xl-2"
        >
          <h4 class="skill-box-title">Japanese</h4>
          <p class="tight-text">
            Native Japanese speaker with a Bachelor of Law from Japan, and
            someone who has always been academically strong.
          </p>
        </div>
        <div
          class="col-8 col-md-10 col-xl-2 p-xl-0 p-2 skill-level-box d-flex flex-column justify-content-around py-xl-3 order-xl-2"
        >
          <div class="skill-level-number-box border rounded text-center">
            100 / 100
          </div>
          <div class="progress">
            <div
              class="progress-bar bg-success"
              role="progressbar"
              style="width: 100%"
              aria-valuenow="25"
              aria-valuemin="0"
              aria-valuemax="100"
            ></div>
          </div>
        </div>
      </div>
    </div>

    
    <!-- DIY Skill -->
    <div class="border border-3 border-dark rounded mt-2 skill-box">
      <div class="row py-1 px-3 h-100">
        <div
          class="col-4 col-md-2 col-xl-2 icon-box d-flex align-items-center justify-content-center order-xl-1"
        >
          <div class="p-4 bg-white text-center rounded">
            <img :src="diyIcon" class="card-img-top w-100" alt="..." />
          </div>
        </div>
        <div
          class="col-12 col-xl-8 p-xl-10 p-2 skill-details-box d-flex flex-column order-3 order-xl-2"
        >
          <h4 class="skill-box-title">DIY</h4>
          <p class="tight-text">
            I’m a hands‑on, practical person, and I even ran a small handyman
            business during the pandemic.
          </p>
        </div>
        <div
          class="col-8 col-md-10 col-xl-2 p-xl-0 p-2 skill-level-box d-flex flex-column justify-content-around py-xl-3 order-xl-2"
        >
          <div class="skill-level-number-box border rounded text-center">
            75 / 100
          </div>
          <div class="progress">
            <div
              class="progress-bar bg-success"
              role="progressbar"
              style="width: 75%"
              aria-valuenow="25"
              aria-valuemin="0"
              aria-valuemax="100"
            ></div>
          </div>
        </div>
      </div>
    </div>

    
    
    <!-- DOCKER / AWS / MySQL Skill -->
    <div class="border border-3 border-dark rounded mt-2 skill-box">
      <div class="row py-1 px-3 h-100">
        <div
          class="col-4 col-md-2 col-xl-2 icon-box d-flex align-items-center justify-content-center order-xl-1"
        >
          <div class="p-4 bg-white text-center rounded">
            <img :src="laptopIcon" class="card-img-top w-100" alt="..." />
          </div>
        </div>
        <div
          class="col-12 col-xl-8 p-xl-10 p-2 skill-details-box d-flex flex-column order-3 order-xl-2"
        >
           <h4 class="skill-box-title">DOCKER / AWS / MySQL</h4>
          <p class="tight-text">
            I gained some experience through my university studies, though my
            practical skills were still limited at that stage.
          </p>
        </div>
        <div
          class="col-8 col-md-10 col-xl-2 p-xl-0 p-2 skill-level-box d-flex flex-column justify-content-around py-xl-3 order-xl-2"
        >
          <div class="skill-level-number-box border rounded text-center">
            2 / 100
          </div>
          <div class="progress">
            <div
              class="progress-bar bg-success"
              role="progressbar"
              style="width: 2%"
              aria-valuenow="25"
              aria-valuemin="0"
              aria-valuemax="100"
            ></div>
          </div>
        </div>
      </div>
    </div>

      
    <!-- PHP (Laravel) Skill -->
    <div class="border border-3 border-dark rounded mt-2 skill-box">
      <div class="row py-1 px-3 h-100">
        <div
          class="col-4 col-md-2 col-xl-2 icon-box d-flex align-items-center justify-content-center order-xl-1"
        >
          <div class="p-4 bg-white text-center rounded">
            <img :src="laravelIcon" class="card-img-top w-100" alt="..." />
          </div>
        </div>
        <div
          class="col-12 col-xl-8 p-xl-10 p-2 skill-details-box d-flex flex-column order-3 order-xl-2"
        >
           <h4 class="skill-box-title">PHP (Laravel)</h4>
          <p class="tight-text">
            I built an event‑booking system at uni with a GPA of 7, while my
            skills were still developing.
          </p>
        </div>
        <div
          class="col-8 col-md-10 col-xl-2 p-xl-0 p-2 skill-level-box d-flex flex-column justify-content-around py-xl-3 order-xl-2"
        >
          <div class="skill-level-number-box border rounded text-center">
            8 / 100
          </div>
          <div class="progress">
            <div
              class="progress-bar bg-success"
              role="progressbar"
              style="width: 8%"
              aria-valuenow="25"
              aria-valuemin="0"
              aria-valuemax="100"
            ></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.skill-box {
  background-color: var(--skill-box);
  display: flex;
  /* flex: 1; */
}
.skill-box-title {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-weight: bold;
}
.tight-text {
  line-height: 1;
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
}
.skill-level-number-box {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-weight: bold;
}
</style>
