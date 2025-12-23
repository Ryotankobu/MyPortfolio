<script setup>
import SectionHeader from "./common/SectionHeader.vue";
import sampleImage from "@/assets/images/bellsprout.png";
import projects from "@/assets/data/projects.json";
import { ref, computed } from "vue";

const modalShowingProjectId = ref("");
const modalContents = computed(() =>
  projects.find((p) => p.id === modalShowingProjectId.value)
);

function getImage(fileName) {
  return new URL(`../assets/images/projectImages/${fileName}`, import.meta.url)
    .href;
}

function modalTargetProject(id) {
  modalShowingProjectId.value = id;
  console.log(modalContents.value);
}

// const truncatedDescriptionArray = ref([])
const truncatedDescription = computed(() => {
  return projects.map(project => {
    if (!project.modalDescription) return ''

    return project.modalDescription.substring(0, 270) + '  .......';
  })
  
}
)
</script>

<template>
  <div id="project" class="section-anchor"></div>
  <div class="project-container">
    <div class="experience-container d-flex flex-column py-5 px-5">
      <SectionHeader
        title="My Projects"
        description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas metus massa, imperdiet eu convallis eu, semper quis est. Pellentesque auctor pharetra lectus. Aenean cursus sem ante, eu elementum quam luctus ut. Nulla imperdiet semper justo sit amet rutrum. Vivamus."
      />
      <div class="project-section-main container-fluid">
        <div class="row g-5">
          <div
            v-for="(project, index) in projects"
            class="col-4"
            :key="project.id || project.title"
          >
            <div
              v-if="!project.isProjectAvailable"
              class="card h-100 border-dark border-3 p-3"
            >
              <div
                class="bg-secondary-subtle h-100 rounded d-flex justify-content-center align-items-center"
              >
                <p class="m-0">Not Available...</p>
              </div>
            </div>
            <div v-else class="card h-100 border-dark border-3">
              <img
                class="card-img-top mx-auto d-block"
                :src="getImage(project.thumbnail)"
                alt="Card image cap"
              />
              <div class="card-body">
                <div
                  class="language-section d-flex flex-row flex-wrap justify-content-between mb-2"
                >
                  <div v-for="budge in project.budges" class="mb-1">
                    <div class="language-box border rounded px-3 bg-light">
                      {{ budge.name }}
                    </div>
                  </div>
                </div>
                <h5 class="card-title">{{ project.title }}</h5>
                <p class="card-text">{{ truncatedDescription[index] }}</p>
                <hr class="border-bottom border-2 border-dark" />
                <div
                  class="project-button-section d-flex flex-row justify-content-between"
                >
                  <button
                    type="button"
                    class="btn btn-success"
                    data-bs-toggle="modal"
                    data-bs-target="#staticBackdrop"
                    @click="modalTargetProject(project.id)"
                  >
                    More Details
                  </button>
                  <div class="project-icon-section">
                    <a
                      :href="project.gitLink"
                      class="btn btn-success me-3"
                      target="_blank"
                      rel="noopener"
                      data-toggle="tooltip"
                      data-placement="bottom"
                      title="GO To GitHub"
                    >
                      <i class="fa-brands fa-github"></i>
                    </a>
                    <a
                      :href="project.deployLink"
                      class="btn btn-success"
                      target="_blank"
                      rel="noopener"
                      data-toggle="tooltip"
                      data-placement="bottom"
                      title="GO To Deployed Page"
                    >
                      <i class="fa-solid fa-desktop"></i>
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Modal -->
  <div
    class="modal fade"
    id="staticBackdrop"
    tabindex="-1"
    aria-labelledby="staticBackdropLabel"
    aria-hidden="true"
  >
    <div class="modal-dialog modal-dialog-scrollable modal-lg">
      <div class="modal-content p-3">
        <div class="modal-body">
          <div class="row" v-if="modalContents">
            <div class="col-12">
              <div class="image-area mb-2">
                <div id="carouselExampleIndicators" class="carousel slide">
                  <div class="carousel-indicators">
                    <button
                      v-for="(eachImage, index) in modalContents.images"
                      :key="index"
                      type="button"
                      data-bs-target="#carouselExampleIndicators"
                      :data-bs-slide-to="index"
                      :class="{ active: index === 0 }"
                      :aria-current="index === 0 ? 'true' : null"
                      :aria-label="`Slide ${index + 1}`"
                    ></button>
                  </div>
                  <div class="carousel-inner">
                    <div
                      class="carousel-item"
                      :class="{ active: index === 0 }"
                      v-for="(eachImage, index) in modalContents.images"
                    >
                      <img
                        :src="getImage(eachImage.imageTitle)"
                        class="d-block w-100"
                        alt="..."
                      />
                    </div>
                  </div>

                  <button
                    class="carousel-control-prev"
                    type="button"
                    data-bs-target="#carouselExampleIndicators"
                    data-bs-slide="prev"
                  >
                    <span
                      class="carousel-control-prev-icon"
                      aria-hidden="true"
                    ></span>
                    <span class="visually-hidden">Previous</span>
                  </button>
                  <button
                    class="carousel-control-next"
                    type="button"
                    data-bs-target="#carouselExampleIndicators"
                    data-bs-slide="next"
                  >
                    <span
                      class="carousel-control-next-icon"
                      aria-hidden="true"
                    ></span>
                    <span class="visually-hidden">Next</span>
                  </button>
                </div>
              </div>
            </div>
            <div class="col-12">
              <!-- modal title -->
              <h1
                class="modal-title fw-bold mb-2 display-5"
                id="staticBackdropLabel"
              >
                {{ modalContents.title }}
              </h1>

              <!-- modal budge area -->
              <div
                class="language-section d-flex flex-row flex-wrap justify-content-between mb-2"
              >
                <div v-for="budge in modalContents.budges" class="mb-1">
                  <div class="language-box border rounded px-3 bg-light">
                    {{ budge.name }}
                  </div>
                </div>
              </div>

              <!-- modal description area -->
              <div class="modal-description-area">
                {{ modalContents.modalDescription }}
              </div>
            </div>
          </div>
        </div>
        
        <!-- modal fotter area -->
        <div class="d-flex justify-content-between mt-3 px-3 bg-light rounded py-2">
          <div class="link-button-area d-flex flex-row">
            <a
              :href="modalContents?.gitLink"
              class="btn btn-success me-3"
              target="_blank"
              rel="noopener"
              data-toggle="tooltip"
              data-placement="bottom"
              title="GO To GitHub"
            >
              <i class="fa-brands fa-github"></i>
            </a>
            <a
              :href="modalContents?.deployLink"
              class="btn btn-success me-3"
              target="_blank"
              rel="noopener"
              data-toggle="tooltip"
              data-placement="bottom"
              title="GO To Deployed Page"
            >
              <i class="fa-solid fa-desktop"></i>
            </a>
            <a
              v-if="modalContents?.sowLink"
              :href="modalContents?.deployLink"
              class="btn btn-warning"
              target="_blank"
              rel="noopener"
              data-toggle="tooltip"
              data-placement="bottom"
              title="View SoW"
            >
              View SoW
            </a>

          </div>
          <div class="close-button-area">
            <button
              type="button"
              class="btn btn-secondary"
              data-bs-dismiss="modal"
            >
              Close
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.card {
  transition: all 0.3s;
  min-height: 300px;
}

.card:hover {
  transform: scale(1.08);
  box-shadow: 5px 5px;
}

.language-box {
  font-family: "Press Start 2P", system-ui;
  font-weight: 200;
  font-style: normal;
  font-size: 0.7rem;
}

.card-title {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 1.3em;
  font-weight: bold;
}

.card-text {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 0.9em;
}

.btn {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 1em;
  font-weight: bold;
}

/* modal */
.modal-title {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
}
.modal-description-area {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
}
</style>
