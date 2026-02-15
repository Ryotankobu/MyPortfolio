<script setup>
  import Button from './common/Button.vue';
  import sampleImage from '@/assets/images/myHeroImage.png';
  import japanFlag from '@/assets/images/japanFlag.png';
</script>

<template>
  <div class="hero-container container-fluid p-md-5 p-3">
    <div class="row d-flex align-items-stretch">
      <div
        class="col-xl-8 col-12 d-flex"
      >
        <div class="card left-card w-100 h-100 border-9" style="background: var(--main-background)">
          <div class="card-body p-4 d-flex flex-column">
            <!-- <h3 class="card-title m-0 p-0">Hi. My name is</h3> -->
            <h1 class="mt-0 lh-1 title-header">Ryota Ando</h1>
            <!-- <h3 class="card-title card-title-change-area mt-2"><span></span></h3> -->

            <h5 class="changeText mt-1">
              <span>
                <span>Graduate Software Developer</span>
                <span>Already in a casual software development role</span>
                <span>10+ years in marketing and client service</span>
              </span>
            </h5>

            <ul class="card-text pt-3">
              <li>Australian permanent resident.</li>
              <li>Bachelor of Information Technology, Griffith University — GPA of 6.2.</li>
              <li>Currently a Graduate Software Developer at Mom’s Friendly Development Company (MFDC), following a successful internship with the team.</li>
              <li>Currently working part‑time as a casino dealer, reinforcing precision, integrity, and disciplined adherence to procedures.</li>
              <li>Core strengths in JavaScript and React; actively expanding front‑end expertise with Vue.js.</li>
              <li>Previous professional experience includes:</li>
                <ul>
                  <li>Client representative at a Japanese trading company (3 yeras).</li>
                  <li>Marketing manager at an international school (6 years - visa sponsored).</li>
                </ul>
              <li>These roles strengthened:
                <ul>
                  <li>Communication and stakeholder management</li>
                  <li>Customer‑focused problem‑solving</li>
                  <li>Cross‑cultural collaboration</li>
                </ul>
              </li>
            </ul>
           
            
            <div class="row mt-auto">
              <div class="col-lg-6 col-md-6 col-12">
                <Button title="My Resume" link="https://drive.google.com/file/d/1t6PuCYUVX6PrNz6i2LbSpijurPvGhiez/view?usp=sharing"/>
              </div>
              <div class="col-lg-6 col-md-6 col-12">
                <Button title="Portfolio SoW" link="https://docs.google.com/document/d/14oJoLES0YOyUHYIma_ij23yTZWWR7mek/edit?usp=sharing&ouid=113567833347978458048&rtpof=true&sd=true"/>
              </div>
             
            </div>
         
          </div>
        </div>
      </div>
      <div class="col-xl-4 offset-xl-0 offset-1 col-10 px-0 ps-2 d-flex">
        <div class="card right-card w-100 h-100" style="background-color: var(--hero-card-yellow);">
          
          <div class="card-body p-4 d-flex flex-column">
            <div class="card-img-container">
              <img :src="sampleImage" class="card-img-top w-100 hero-image mx-auto d-block border border-2 border-dark" alt="..." />
              <div class="skill-text-container w-100 p-1">
                <p class="skill-box bg-success p-2 rounded-circle">React</p>
                <p class="skill-box bg-success p-2 rounded-circle">Vue.js</p>
                <p class="skill-box bg-success p-2 rounded-circle">HTML/CSS</p>
                <p class="skill-box bg-success p-2 rounded-circle">Bootstrap</p>
              </div>

            </div>
            
            <div class="border rounded mt-4 mb-3 card-info">
              <div class="row p-3">
                <div class="col-6">
                  <h4 class="my-card-title">
                    Australia Visa: 
                  </h4>
                </div>
                <div class="col-6">
                  <h4 class="my-card-title">
                    Permanent Visa
                  </h4>
                </div>
              </div>
            </div>
            <div class="border rounded mt-1 mb-3 card-info">
              <div class="row p-3">
                <div class="col-6">
                  <h4 class="my-card-title">
                    Nationality: 
                  </h4>
                </div>
                <div class="col-6">
                  <div class="d-flex flex-row align-items-center">
                    <h4 class="my-card-title">
                    Japan
                    </h4>
                    <img :src="japanFlag" class="country-icon ms-4" alt="..." />
                  </div>
                  
                </div>
              </div>
            </div>
          
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.hero-container {
}
.card-img-container {
  position: relative;
}
.skill-text-container {
  position: absolute;
  top: 5px;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-around;
  gap: 10px;
}
.skill-box {
  flex: 1;
  text-align: center;
  opacity: 0.9;
   font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 700;
  font-style: normal;
  font-size: 0.9em;
  color: white;
  border-style: solid;
  border-color: black;
  
}

.hero-image {
  width: 100%;
  height: 100%;
  object-fit: cover; 
  transition: all .3s ease-in-out;
}
/* .hero-image:hover {
  transform: scale(1.05);
  box-shadow: 5px 5px var(--shadow-color);
} */
.right-card {
  box-shadow: 10px 12px  var(--shadow-color);
  /* float: left; */
  transform: rotate(2deg);
}
.card-title {
  font-family: "Bungee", sans-serif;
  font-weight: 400;
  font-style: normal;
}
.title-header {
  font-family: "Bungee", sans-serif;
  font-weight: 400;
  font-style: normal;
  font-size: 6em;
  transform: translateX(-0.06em);


}
.changeText span span {
  font-family: "Bungee", sans-serif;
  font-weight: 400;
  font-style: normal;
}
.card-title-change-area span:after {
  content: '(Graduate Software Developer)';
  animation: words 5s infinite;
}
@keyframes words {
  0%, 33% {
    content: '(Graduate Software Developer)';
    color: red;
    background-color: blue;
  }
  34%, 66% {
    content: '(Already in a casual software development role)';
    color: red;
    background-color: yellow;
  }
  67%, 100% {
    content: 'third';
    color: red;
    background-color: green;
  }
}
.card-text {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 1.1em;
}
.left-card {
  box-shadow: 10px 12px  var(--shadow-color);
}
.card-info {
  transition: all .3s ease-in-out;

}
/* .card-info:hover {
  transform: scale(1.05);
  box-shadow: 5px 5px var(--shadow-color);

} */
.border-9 {
  border-width: 9px !important;
}
.country-icon {
  height: 2em;     
  width: auto;     
  margin-left: 8px; 
}

.changeText > span {
  position: relative;
  display: inline-block;
  vertical-align: bottom;
  overflow: hidden;
  height: 1.25em;
}
.changeText > span > span {
  display: block;
  animation: anim 15s infinite ease;
}
@keyframes anim {
  0% {
    transform: translateY(0%);
  }
  33% {
    transform: translateY(0%);
  }
  66% {
    transform: translateY(-100%);
  }
  100% {
    transform: translateY(-200%);
  }
  
}
.my-card-title {
 font-family: "Luckiest Guy", cursive;
  font-weight: 400;
  font-style: normal;
}


@media (max-width: 576px) {
  .changeText span {
    min-height: 70px;
  }
  .title-header {
    font-size: 4em;
  }
}

</style>
