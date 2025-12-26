<script setup>
  import { ref, onMounted, onBeforeUnmount } from 'vue'
import SectionHeader from "./common/SectionHeader.vue";
import TextMarquee from "./common/TextMarquee.vue";
import workExperienceBackground from "../assets/images/windowGreen.png";
// icons for SectionHeader
import icon1 from '@/assets/images/bellsprout.png'
import icon2 from '@/assets/images/bellsprout.png'
import icon3 from '@/assets/images/bellsprout.png'

const workExperienceCardRef = ref(null)
const studyExperienceCardRef = ref(null)

const workExperienceCardVisible = ref(false)
const studyExperienceCardVisible = ref(false)

let observer = null

onMounted(() => {
  observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (!entry.isIntersecting) return

        if (entry.target === workExperienceCardRef.value) {
          workExperienceCardVisible.value = true
          observer.unobserve(entry.target) // only animate once
        }
        if (entry.target === studyExperienceCardRef.value) {
          studyExperienceCardVisible.value = true
          observer.unobserve(entry.target)
        }
      })
    },
    {
      threshold: 0.3, // trigger when ~30% of the column is visible
    }
  )

  if (workExperienceCardRef.value) observer.observe(workExperienceCardRef.value)
  if (studyExperienceCardRef.value) observer.observe(studyExperienceCardRef.value)
})

onBeforeUnmount(() => {
  if (!observer) return
  if (workExperienceCardRef.value) observer.unobserve(workExperienceCardRef.value)
  if (studyExperienceCardRef.value) observer.unobserve(studyExperienceCardRef.value)
})

const leftIcons = [
  { src: icon1, left: '30%', top: '10%', transform: 'rotate(-20deg)' },
  { src: icon2, left: '55%', top: '45%', transform: 'rotate(20deg)' },
  { src: icon3, left: '5%', top: '50%', transform: 'rotate(10deg)' },
]

const rightIcons = [
  { src: icon1, left: '60%', top: '50%', transform: 'rotate(30deg)' },
  { src: icon2, left: '10%', top: '30%', transform: 'rotate(-20deg)' },
  { src: icon3, left: '45%', top: '10%', transform: 'rotate(10deg)' },
]


</script>

<template>
  <div id="experience" class="section-anchor"></div>
  <div class="experience-container d-flex flex-column py-5 px-5">
    <SectionHeader
      title="What I experienced"
      description="My journey combines substantial professional experience with focused academic study. These experiences — both in the workplace and at university — have shaped the way I think, communicate, and build as a developer."
    :left-icons="leftIcons"
    :right-icons="rightIcons"
      />
    <div
      class="experiencce-section-main container-fluid flex-grow-1 p-0 d-flex flex-column"
    >

      <!-- work related scroll section -->
      <div
        class="card work-experience-card mt-4 d-flex flex-column border border-5 border-dark align-items-center p-4 mb-4"
        ref="workExperienceCardRef"
        :class="{'work-experience-card--visible': workExperienceCardVisible}"
      >
        <!-- <img :src="workExperienceBackground" class="work-bg-img" alt="" /> -->
        <h1 class="mb-4 pt-3 display-4 fw-bold">Work</h1>
        <div class="list-and-scroll d-flex flex-row justify-content-between">
          <div id="work-list" class="list-group pe-2">
            <a
              class="list-group-item list-group-item-action border-3 rounded border-dark mb-2 bg-warning-subtle"
              href="#list-item-1"
              >Junior Software Developer
              <br />
              <span style="font-size: 0.9rem"
                >(Mom's Friendly Development Company)</span
              ></a
            >
            <a
              class="list-group-item list-group-item-action border-3 rounded border-dark mb-2 bg-success-subtle"
              href="#list-item-2"
              >Table Games Dealer
              <br />
              <span style="font-size: 0.9rem">(The Star Gold Coast)</span></a
            >
            <a
              class="list-group-item list-group-item-action border-3 rounded border-dark mb-2 bg-danger-subtle"
              href="#list-item-3"
              >Marketing and Client Service Manager
              <br />
              <span style="font-size: 0.9rem"
                >(Inforum Education Australia)</span
              >
            </a>

            <a
              class="list-group-item list-group-item-action border-3 rounded border-dark mb-2 bg-info-subtle"
              href="#list-item-4"
              >Sales Specialist
              <br />
              <span style="font-size: 0.9rem"
                >(Japan Pulp and Paper Company Limited)</span
              >
            </a>
          </div>

          <div
            id="work-scrollspy"
            class="scrollspy-area flex-grow-1 overflow-auto border border-3 border-dark rounded p-2"
            data-bs-spy="scroll"
            data-bs-target="#work-list"
            data-bs-offset="80"
            tabindex="0"
            style="background-color: white"
          >
            <h2 id="list-item-1" class="bg-warning-subtle px-2 pt-2">
              Mum's Friendly Development Company (MFDC)<br />
              <span style="font-size: 0.95rem"
                >Graduate Software Developer (June 2025 to Current)</span
              >
            </h2>

            <div class="bg-warning-subtle p-2">
              <!-- BA related card -->
              <div class="card w-100 my-2 bg-white">
                <div class="card-body">
                  <p class="card-title text-decoration-underline">
                    Business Analysis & Coordination
                  </p>
                  <ul>
                    <li>
                      Supported weekly sprint planning and task prioritisation
                    </li>
                    <li>
                      Tracked issue status and progress through regular
                      communication with team members
                    </li>
                    <li>
                      Assisted in preparing technical documentation, including
                      Statements of Work (SoW) and progress reports
                    </li>
                  </ul>
                </div>
              </div>
              <!-- Technical work related card -->
              <div class="card w-100 my-2 bg-white">
                <div class="card-body">
                  <p class="card-title text-decoration-underline">
                    Technical Contributions
                  </p>
                  <ul>
                    <li>
                      Designed and implemented new system features, including
                      additional form pages, tab-based navigation, and extended
                      workflows
                    </li>
                    <li>
                      Built a risk matrix with calculation logic to support
                      structured risk assessment and data-driven decision-making
                    </li>
                    <li>
                      Developed data visualisations such as treemaps with
                      interactive tooltips by aggregating existing assessment
                      data
                    </li>
                    <li>
                      Contributed to front-end development using Vue.js, HTML,
                      CSS, and Bootstrap
                    </li>
                  </ul>
                </div>
              </div>

              <div class="accordion" id="accordionExample">
                <div class="accordion-item">
                  <h4 class="accordion-header" id="headingOne">
                    <button
                      class="accordion-button bg-primary-subtle border border-dark border-2"
                      type="button"
                      data-bs-toggle="collapse"
                      data-bs-target="#collapseOne"
                      aria-expanded="true"
                      aria-controls="collapseOne"
                    >
                      Issues/Tickets I Actually Compeletd (not all / order of
                      difficulty)
                    </button>
                  </h4>
                  <div
                    id="collapseOne"
                    class="accordion-collapse collapse"
                    aria-labelledby="headingOne"
                    data-bs-parent="#accordionExample"
                  >
                    <div class="accordion-body">
                      <strong>FOZ-1022 Automated Data Collection<br /></strong>
                      Created a new UI form page by extending the existing
                      route, as well as using the param to retrieve the existing
                      user filled data for the new form.<br />
                      <strong>FOZ-1033 Risk Matrix<br /></strong>
                      After user defines a risk levels for multiple categoried,
                      I implemented a logic to calcilate the combined risk
                      level, and made a logic of displaying the result risk
                      volume with client defined style coloured idication.<br />
                      <strong
                        >FOZ-1036 Restrictive Precence Listing<br
                      /></strong>
                      Implemented a bootstrap tab in the existing form and made
                      a new component for the newly created tab to display a
                      necessary table.<br />
                      <strong
                        >FOZ-1035 Medical and Prescription Listing<br
                      /></strong>
                      Similar to above (tab creation), added a new text input
                      area by entending the existing schema file (where defines
                      the data structure) and created a new UI for the
                      textarea.<br />
                      <strong>.<br /></strong>
                      <strong>.<br /></strong>
                      <strong>.<br /></strong>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <hr class="border-bottom border-2 border-dark" />
            <!-- work item2 -->
            <h2 id="list-item-2" class="bg-success-subtle px-2 pt-2">
              The Star Gold Coast<br />
              <span style="font-size: 0.95rem"
                >Table Games Dealer (October 2022 to Current)</span
              >
            </h2>
            <div class="bg-success-subtle px-2 pt-2 pb-2">
              <ul>
                <li>
                  Dealt Roulette, Baccarat, and Blackjack games with strict
                  compliance to casino regulations, gaming laws, and operational
                  procedures, ensuring a fair and secure gaming environment.
                </li>
                <li>
                  Demonstrated strong multitasking skills by efficiently
                  managing chip transactions, monitoing multiple players,
                  maintaining game flow, and addressing customer inquiries
                  simultaneously.
                </li>
                <li>
                  Accurately handled large volumes of chips and cash under
                  high-pressure conditions, maintaining focus and adherence to
                  strict internal controls.
                </li>
                <li>
                  Collaborated with supervisors and security teams to address
                  potential risks, resolve disputes, and ensure a smooth,
                  compliant gaming floor operation.
                </li>
              </ul>
            </div>
            <hr class="border-bottom border-2 border-dark" />
            <!-- work item3 -->
            <h2 id="list-item-3" class="bg-danger-subtle px-2 pt-2">
              Inforum Education Australia <br />
              <span style="font-size: 0.95rem"
                >Marketing and Client Service Manager (Apr 2015 to Sep 2021 -
                6yes 6 mos)</span
              >
            </h2>
            <div class="bg-danger-subtle px-2 pt-2 pb-2">
              <ul>
                <li>
                  Managed communication channels with Japanese agents locally
                  and overseas, attending delivering presentations
                </li>
                <li>
                  Developed relationships with Japanese agents and prospective
                  students to ensure seamless service delivery.
                </li>
                <li>
                  Provided counselling services for Japanese students,
                  addressing day-to-day issues effectively.
                </li>
                <li>
                  Corresponded with agents and students, primarily based in
                  Japan, to ensure their requirements were met.
                </li>
              </ul>
            </div>
            <hr class="border-bottom border-2 border-dark" />
            <!-- work item4 -->
            <h2 id="list-item-4" class="bg-info-subtle px-2 pt-2">
              Japan Pulp and Paper Company Limited<br />
              <span style="font-size: 0.95rem"
                >Sales Specialist (Apr 2012 to Mar 2015 - 3yes)</span
              >
            </h2>
            <div class="bg-info-subtle px-2 pt-2 pb-2">
              <ul>
                <li>
                  Maintained good relationship with all clients through
                  effective communication, leadership, discipline and motivation
                </li>
                <li>Analysed sales documents, and created client lists</li>
                <li>
                  Fostered collaboration with internal purchasing departments to
                  streamline workflows.
                </li>
                <li>
                  Prepared impactful presentation materials for client
                  proposals.
                </li>
                <li>
                  Worked with implementation teams to create tailored
                  client-specific solutions.
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>


      <!-- study related scroll section -->
      <div
        ref="studyExperienceCardRef"
        class="card study-experience-card mt-4 d-flex flex-column border border-5 border-dark align-items-center p-4"
        :class="{'study-experience-card--visible': studyExperienceCardVisible}"
        >
        <h1 class="mb-4 pt-3 display-4 fw-bold">Study</h1>
        <div class="list-and-scroll d-flex flex-row justify-content-between">
          <div id="study-list" class="list-group pe-2">
            <a
              class="list-group-item study-list-group-item-action border-3 rounded border-dark mb-2 bg-warning-subtle"
              href="#study-list-item-1"
              >Bachelor of Information Technology
              <br />
              <span style="font-size: 0.9rem">(Griffith University)</span>
            </a>
            <a
              class="list-group-item study-list-group-item-action border-3 rounded border-dark mb-2 bg-info-subtle"
              href="#study-list-item-2"
              >Bachelor of Law
              <br />
              <span style="font-size: 0.9rem">(University of Toyama)</span>
            </a>
          </div>

          <div
            id="study-scrollspy"
            class="scrollspy-area flex-grow-1 overflow-auto border border-3 border-dark rounded p-2"
            data-bs-spy="scroll"
            data-bs-target="#study-list"
            data-bs-offset="80"
            tabindex="0"
            style="background-color: white"
          >
            <h2 id="study-list-item-1" class="bg-warning-subtle px-2 pt-2">
              Bachelor of Information Technology<br />
              <span style="font-size: 0.95rem"
                >- Griffith university (2022 - 2025)</span
              ><br />
              <span style="font-size: 0.95rem"
                >- Major: Information Technology</span
              ><br />
              <span style="font-size: 0.95rem"
                >- Grade Point Average: 6.2 (Scale 1 -7, 7 being the
                highest)</span
              ><br />
            </h2>
            <div class="bg-warning-subtle p-2">
              <!-- Team based projects card -->
              <div class="card w-100 my-2 bg-white">
                <div class="card-body">
                  <p class="card-title text-decoration-underline">
                    Team-Based University Project
                  </p>
                  <ul>
                    <li>
                      Developed a Python desktop application to fetch data from
                      an Excel file as a database.
                    </li>
                    <li>
                      Created a software Lifecycle Development plan for a local
                      business
                    </li>
                    <li>
                      Configured an AWS Docker environment for a provided online
                      platform (local business homepage).
                    </li>
                  </ul>
                </div>
              </div>
              <!-- Individual projects card -->
              <div class="card w-100 my-2 bg-white">
                <div class="card-body">
                  <p class="card-title text-decoration-underline">
                    Individual University Project
                  </p>
                  <ul>
                    <li>
                      Developed an online chat system as a full-stack project
                      using the MEAN stack.
                    </li>
                    <li>
                      Built a React project to fetch API-based photos according
                      to user interactions.
                    </li>
                    <li>
                      Created a board game using JavaScript flamework p5.js.
                    </li>
                    <li>Designed a homepage using HTML and CSS</li>
                  </ul>
                </div>
              </div>
            </div>
            <hr class="border-bottom border-2 border-dark" />
            <h2 id="study-list-item-2" class="bg-info-subtle px-2 pt-2 pb-3">
              Bachelor of Law<br />
              <span style="font-size: 0.95rem"
                >- University of Toyama, Japan (2006 - 2012)</span
              ><br />
             
             
            </h2>

          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.experience-container {
  background-color: var(--experience-section-background);
}
h1 {
  font-family: "Bungee", sans-serif;
  font-weight: 400;
  font-style: normal;
}
h2 {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 1.8em;
  font-weight: bold;
}
h4 {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 1.3em;
  font-weight: bold;
}
p {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 1.1em;
}
li {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 1.1em;
}

.scrollspy-area {
  max-height: 500px;
}
.scrollspy-area h4[id] {
  scroll-margin-top: 80px;
}
.list-group-item {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 1.1em;
  font-weight: bold;
}
.list-group-item.active {
  color: rgb(246, 82, 17);
  box-shadow: 2px 2px #000000;
}
.list-group-item:hover {
  transform: scale(1.02);
  box-shadow: 2px 2px #000000;
}
.accordion-button:hover {
  transform: scale(1.02);
  box-shadow: 2px 2px #000000;
}
.work-experience-card {
  position: relative;
  background-color: var(--work-experience-background);
  box-shadow: 10px 12px var(--shadow-color);
  opacity: 0;
  transform: translateX(-40px);
}
.work-experience-card--visible.work-experience-card {
  animation: slideInLeft 0.8s ease-out forwards;
 
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

.work-bg-img {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: fill;
  z-index: 0;
}
.work-experience-card > *:not(img) {
  z-index: 1; 
}

#work-list {
  width: 30%;
}
#work-scrollspy {
  width: 70%;
}
#work-scrollspy {
  scroll-padding-top: 80px;
}





.study-experience-card {
  background-color: var(--study-experience-background);
  box-shadow: 10px 12px var(--shadow-color);
  opacity: 0;
  transform: translateX(-40px);
}
.study-experience-card--visible.study-experience-card {
  animation: slideInLeft 0.8s ease-out forwards;
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
#study-list {
  width: 30%;
}
#study-scrollspy {
  width: 70%;
}
#study-scrollspy {
  scroll-padding-top: 80px;
}
.accordion-button {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 0.9em;
}
</style>
