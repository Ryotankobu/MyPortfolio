<script setup>
    import sampleImage from "@/assets/images/bellsprout.png";
    import reactIcon from "@/assets/images/reactIcon.svg.png";
    import vueIcon from "@/assets/images/vueIcon.png";
    import reactNativeIcon from "@/assets/images/reactNativeIcon.svg";
    import htmlcssIcon from "@/assets/images/htmlcssIcon.png";
</script>
<template>
    <div class="d-flex flex-column h-100 mt-3">

              <!-- React skill -->
              <div class="border border-3 border-dark rounded mt-2 skill-box">
                <div class="row py-1 px-3 h-100">
                 <div
                    class="col-4 col-md-2 col-xl-2 icon-box d-flex align-items-center justify-content-center order-xl-1"
                  >
                  <div class="p-4 bg-white text-center rounded">
                    <img
                       :src="reactIcon"
                      class="card-img-top w-100"
                      alt="..."
                    />

                  </div>
                    
                  </div>
                  <div
                    class="col-12 col-xl-8 p-xl-10 p-2 skill-details-box d-flex flex-column order-3 order-xl-2"
                  >
                   <h4 class="skill-box-title">React</h4>
                    <p class="tight-text">
                      I completed several React courses (Codecademy, Scrimba, YouTube) and put those skills into practice by building a movie‑finder app using the TMDb API, focusing on UI clarity and efficient API integration.
                    </p>
                  </div>
                  <div
                    class="col-8 col-md-10 col-xl-2 p-xl-0 p-2 skill-level-box d-flex flex-column justify-content-around py-xl-3 order-xl-2"
                  >
                    <div
                      class="skill-level-number-box border rounded text-center"
                    >
                      25 / 100
                    </div>
                      <div class="progress">
                        <div
                          class="progress-bar bg-success"
                          role="progressbar"
                          style="width: 25%"
                          aria-valuenow="25"
                          aria-valuemin="0"
                          aria-valuemax="100"
                        ></div>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Vue skill -->
              <div class="border border-3 border-dark rounded mt-2 skill-box">
                <div class="row py-1 px-3 h-100">
                 <div
                    class="col-4 col-md-2 col-xl-2 icon-box d-flex align-items-center justify-content-center order-xl-1"
                  >
                  <div class="p-4 bg-white text-center rounded">
                    <img
                       :src="vueIcon"
                      class="card-img-top w-100"
                      alt="..."
                    />
                  </div>
                  </div>
                  <div
                    class="col-12 col-xl-8 p-xl-10 p-2 skill-details-box d-flex flex-column order-3 order-xl-2"
                  >
                   <h4 class="skill-box-title">Vue.js</h4>
                    <p class="tight-text">
                     I use Vue.js in MFDC projects to deliver client‑focused features, supported by ongoing learning through Scrimba and YouTube. This portfolio is also built with Vue, giving me hands‑on practice with the framework.
                    </p>
                  </div>
                  <div
                    class="col-8 col-md-10 col-xl-2 p-xl-0 p-2 skill-level-box d-flex flex-column justify-content-around py-xl-3 order-xl-2"
                  >
                    <div
                      class="skill-level-number-box border rounded text-center"
                    >
                      22 / 100
                    </div>
                      <div class="progress">
                        <div
                          class="progress-bar bg-success"
                          role="progressbar"
                          style="width: 22%"
                          aria-valuenow="25"
                          aria-valuemin="0"
                          aria-valuemax="100"
                        ></div>
                    </div>
                  </div>
                </div>
              </div>

              
              <!-- React Native skill -->
              <div class="border border-3 border-dark rounded mt-2 skill-box">
                <div class="row py-1 px-3 h-100">
                 <div
                    class="col-4 col-md-2 col-xl-2 icon-box d-flex align-items-center justify-content-center order-xl-1"
                  >
                  <div class="p-4 bg-white text-center rounded">
                    <img
                      :src="reactNativeIcon"
                      class="card-img-top w-100"
                      alt="..."
                    />
                  </div>
                  </div>
                  <div
                    class="col-12 col-xl-8 p-xl-10 p-2 skill-details-box d-flex flex-column order-3 order-xl-2"
                  >
                   <h4 class="skill-box-title">React Native</h4>
                    <p class="tight-text">
                      As part of a university project, I built a full shopping app in React Native, implementing clean UI, navigation, and data handling. The project earned a perfect 100/100, highlighting the quality and reliability of my work.
                    </p>
                  </div>
                  <div
                    class="col-8 col-md-10 col-xl-2 p-xl-0 p-2 skill-level-box d-flex flex-column justify-content-around py-xl-3 order-xl-2"
                  >
                    <div
                      class="skill-level-number-box border rounded text-center"
                    >
                      24 / 100
                    </div>
                      <div class="progress">
                        <div
                          class="progress-bar bg-success"
                          role="progressbar"
                          style="width: 24%"
                          aria-valuenow="25"
                          aria-valuemin="0"
                          aria-valuemax="100"
                        ></div>
                    </div>
                  </div>
                </div>
              </div>

              <!-- HTML / CSS Skill -->
              <div class="border border-3 border-dark rounded mt-2 skill-box">
                <div class="row py-1 px-3 h-100">
                 <div
                    class="col-4 col-md-2 col-xl-2 icon-box d-flex align-items-center justify-content-center order-xl-1"
                  >
                  <div class="p-4 bg-white text-center rounded">
                    <img
                      :src="htmlcssIcon"
                      class="card-img-top w-100"
                      alt="..."
                    />

                  </div>
                    
                  </div>
                  <div
                    class="col-12 col-xl-8 p-xl-10 p-2 skill-details-box d-flex flex-column order-3 order-xl-2"
                  >
                   <h4 class="skill-box-title">HTML & CSS (Bootstrap)</h4>
                    <p class="tight-text">
                     Strong foundation in semantic HTML, responsive CSS, and Bootstrap. I focus on clean structure, accessibility, and maintainable styling, and this portfolio is built with Bootstrap to apply those principles in practice.
                    </p>
                  </div>
                  <div
                    class="col-8 col-md-10 col-xl-2 p-xl-0 p-2 skill-level-box d-flex flex-column justify-content-around py-xl-3 order-xl-2"
                  >
                    <div
                      class="skill-level-number-box border rounded text-center"
                    >
                      38 / 100
                    </div>
                      <div class="progress">
                        <div
                          class="progress-bar bg-success"
                          role="progressbar"
                          style="width: 38%"
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