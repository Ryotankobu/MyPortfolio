<script setup>
import SectionHeader from "./common/SectionHeader.vue";
import sampleImage from "@/assets/images/bellsprout.png";
</script>

<template>
  <div id="about" class="section-anchor"></div>
  <div class="about-container d-flex flex-column py-5">
    <SectionHeader
      title="Know More About Me"
      description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas metus massa, imperdiet eu convallis eu, semper quis est. Pellentesque auctor pharetra lectus. Aenean cursus sem ante, eu elementum quam luctus ut. Nulla imperdiet semper justo sit amet rutrum. Vivamus."
    />
    <div class="about-section-main container-fluid bg-success flex-grow-1">
      <div class="row h-100">
        <div class="col-4 bg-primary p-0 pe-2">
          <div
            class="card p-4 h-100 d-flex flex-column justify-content-between"
          >
            <div class="border rounded d-flex align-items-center justify-content-center py-2">
              <p class="m-0">section2</p>
            </div>
            <img
              :src="sampleImage"
              class="card-img-top w-75 hero-image mx-auto d-block"
              alt="..."
            />
            <div class="border rounded d-flex align-items-center justify-content-center py-2">
              <p class="m-0">section2</p>
            </div>
          </div>
        </div>

        <div class="col-8 h-100 bg-secondary p-0 ps-2">
          <div
            class="card h-100 p-4 d-flex flex-column justify-content-between"
          >
            <ul class="nav nav-pills nav-fill">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#"
                  >Active</a
                >
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Much longer nav link</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Link</a>
              </li>
              <li class="nav-item">
                <a class="nav-link disabled" aria-disabled="true">Disabled</a>
              </li>
            </ul>

            <div class="d-flex flex-column h-100 mt-3">

              <div class="border rounded mt-2 skill-box">
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
                    <h4>aaaaaaaaaaaa</h4>
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
                      aaa
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


              <div class="border rounded mt-2 skill-box">
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
                    <h4>aaaaaaaaaaaa</h4>
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
                      aaa
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


              <div class="border rounded mt-2 skill-box">
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
                    <h4>aaaaaaaaaaaa</h4>
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
                      aaa
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


              <div class="border rounded mt-2 skill-box">
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
                    <h4>aaaaaaaaaaaa</h4>
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
                      aaa
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
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.about-container {
  background-color: navajowhite;
  scroll-margin-top: 80px;
}
.about-section-main {
}
.skill-box {
  flex: 1;
}
.tight-text {
  line-height: 1;
}
</style>
