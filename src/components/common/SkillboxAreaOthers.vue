<script setup>
    import sampleImage from "@/assets/images/bellsprout.png";
</script>
<template>
    <div class="d-flex flex-column h-100 mt-3">
              <div class="border border-3 border-dark rounded mt-2 skill-box" style="background-color: var(--skill-box);">
                <div class="row py-1 px-3 h-100">
                  <div
                    class="col-2 p-0 icon-box d-flex align-items-center justify-content-center"
                  >
                    <img
                      :src="sampleImage"
                      class="card-img-top w-75"
                      alt="..."
                    />
                  </div>
                  <div
                    class="col-8 p-0 pe-2 skill-details-box d-flex flex-column"
                  >
                    <h4 class="skill-box-title">This is an Other skills area</h4>
                    <p class="tight-text">
                      aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
                    </p>
                  </div>
                  <div
                    class="col-2 p-0 skill-level-box d-flex flex-column justify-content-around py-3"
                  >
                    <div
                      class="skill-level-number-box border rounded text-center"
                    >
                      20 / 99
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


              <div class="border border-3 border-dark rounded mt-2 skill-box" style="background-color: var(--skill-box);">
                <div class="row py-1 px-3 h-100">
                  <div
                    class="col-2 p-0 icon-box d-flex align-items-center justify-content-center"
                  >
                    <img
                      :src="sampleImage"
                      class="card-img-top w-75"
                      alt="..."
                    />
                  </div>
                  <div
                    class="col-8 p-0 pe-2 skill-details-box d-flex flex-column"
                  >
                    <h4 class="skill-box-title">aaaaaaaaaaaa</h4>
                    <p class="tight-text">
                      aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
                    </p>
                  </div>
                  <div
                    class="col-2 p-0 skill-level-box d-flex flex-column justify-content-around py-3"
                  >
                    <div
                      class="skill-level-number-box border rounded text-center"
                    >
                      20 / 99
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


              <div class="border border-3 border-dark rounded mt-2 skill-box" style="background-color: var(--skill-box);">
                <div class="row py-1 px-3 h-100">
                  <div
                    class="col-2 p-0 icon-box d-flex align-items-center justify-content-center"
                  >
                    <img
                      :src="sampleImage"
                      class="card-img-top w-75"
                      alt="..."
                    />
                  </div>
                  <div
                    class="col-8 p-0 pe-2 skill-details-box d-flex flex-column"
                  >
                    <h4 class="skill-box-title">aaaaaaaaaaaa</h4>
                    <p class="tight-text">
                      aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
                    </p>
                  </div>
                  <div
                    class="col-2 p-0 skill-level-box d-flex flex-column justify-content-around py-3"
                  >
                    <div
                      class="skill-level-number-box border rounded text-center"
                    >
                      20 / 99
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


              <div class="border border-3 border-dark rounded mt-2 skill-box" style="background-color: var(--skill-box);">
                <div class="row py-1 px-3 h-100">
                  <div
                    class="col-2 p-0 icon-box d-flex align-items-center justify-content-center"
                  >
                    <img
                      :src="sampleImage"
                      class="card-img-top w-75"
                      alt="..."
                    />
                  </div>
                  <div
                    class="col-8 p-0 pe-2 skill-details-box d-flex flex-column"
                  >
                    <h4 class="skill-box-title">aaaaaaaaaaaa</h4>
                    <p class="tight-text">
                      aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
                    </p>
                  </div>
                  <div
                    class="col-2 p-0 skill-level-box d-flex flex-column justify-content-around py-3"
                  >
                    <div
                      class="skill-level-number-box border rounded text-center"
                    >
                      20 / 99
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
            </div>
</template>
<style scoped>
    .skill-box-title {
  font-family: "Luckiest Guy", cursive;
  font-weight: 400;
  font-style: normal;

}
.tight-text {
  line-height: 1;
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
}

</style>