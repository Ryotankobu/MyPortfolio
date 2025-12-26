<script setup>
  import { ref, onMounted, onBeforeUnmount } from 'vue'
import SectionHeader from "./common/SectionHeader.vue";
import sampleImage from "@/assets/images/bellsprout.png";
// icons for SectionHeader
import icon1 from '@/assets/images/bellsprout.png'
import icon2 from '@/assets/images/bellsprout.png'
import icon3 from '@/assets/images/bellsprout.png'

const contactDetailsBoxRef = ref(null)
const contactFormBoxRef = ref(null)

const contactDetailsBoxVisible = ref(false)
const contactFormBoxVisible = ref(false)

let observer = null

onMounted(() => {
  observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (!entry.isIntersecting) return

        if (entry.target === contactDetailsBoxRef.value) {
          contactDetailsBoxVisible.value = true
          observer.unobserve(entry.target) // only animate once
        }
        if (entry.target === contactFormBoxRef.value) {
          contactFormBoxVisible.value = true
          observer.unobserve(entry.target)
        }
      })
    },
    {
      threshold: 0.3, // trigger when ~30% of the column is visible
    }
  )

  if (contactDetailsBoxRef.value) observer.observe(contactDetailsBoxRef.value)
  if (contactFormBoxRef.value) observer.observe(contactFormBoxRef.value)
})

onBeforeUnmount(() => {
  if (!observer) return
  if (contactDetailsBoxRef.value) observer.unobserve(contactDetailsBoxRef.value)
  if (contactFormBoxRef.value) observer.unobserve(contactFormBoxRef.value)
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
  <div id="contact" class="section-anchor"></div>
  <div class="contact-container">
    <div class="experience-container d-flex flex-column py-5 px-5">
      <SectionHeader 
      title="Contact Me"
      description="If you’d like to get in touch, I’d be happy to hear from you. Whether you have an opportunity to discuss, feedback to share, or simply want to connect, feel free to reach out through the form below. I’ll respond as soon as I can" 
      :left-icons="leftIcons"
      :right-icons="rightIcons"/>
      <div class="contact-section-main container-fluid">
        <div class="row">
          <div class="col-5 ps-0">
            <!-- left side area -->
            <div
              class="card contact-details-box border rounded border-3 border-dark p-3 d-flex flex-column justify-content-between"
              ref="contactDetailsBoxRef"
              :class="{ 'contact-details-box--visible': contactDetailsBoxVisible }"
              >
              
              <div class="contact-explanation-area w-100">
                <h3 class="card-title">Ryota Ando</h3>
                <p class="card-text">
                  Below are my contact details. Feel free to reach out for collaborations, opportunities, or even just a
                  friendly chat. I’m always happy to connect.
                </p>
              </div>
              <div class="contact-items-area mt-3">
                <!-- contact item1 -->
                <div class="contact-item border border-dark border-2 rounded mb-2 bg-success-subtle">
                  <div class="row p-2">
                    <div class="col-2 p-0 icon-box d-flex align-items-center justify-content-center ">
                      <i class="fa-solid fa-envelope fa-2x"></i>
                    </div>
                    <div class="col-10 p-0 d-flex flex-column justify-content-between ps-2">
                      <h4 class="m-0">Email</h4>
                      <p class="m-0">ucp4fya7@yahoo.co.jp</p>
                    </div>
                  </div>
                </div>

                <!-- contact item2 -->
                <div class="contact-item border border-dark border-2 rounded mb-2 bg-success-subtle">
                  <div class="row p-2">
                    <div class="col-2 p-0 icon-box d-flex align-items-center justify-content-center">
                      <i class="fa-solid fa-phone fa-2x"></i>
                    </div>
                    <div class="col-10 p-0 d-flex flex-column justify-content-between ps-2">
                      <h4 class="m-0">Phone</h4>
                      <p class="m-0">0401 862 572</p>
                    </div>
                  </div>
                </div>

                <!-- contact item3  -->
                <div class="contact-item border border-dark border-2 rounded mb-2 bg-success-subtle">
                  <div class="row p-2 ">
                    <div class="col-2 p-0 icon-box d-flex align-items-center justify-content-center">
                      <i class="fa-solid fa-location-dot fa-2x"></i>
                    </div>
                    <div class="col-10 p-0 d-flex flex-column justify-content-between ps-2">
                      <h4 class="m-0">Location</h4>
                      <p class="m-0">Gold Coast, Australia</p>
                    </div>
                  </div>
                </div>
              </div>
              <div class="contact-icons-area d-flex flex-column p-2">
                <p class="m-0 mb-1">Let’s connect — you can also grab my resume below</p>
                <div class="icon-box">
                  <div class="row">
                    <div class="col-1">
                      <a href="https://www.google.com"  target="_blank" rel="noopener"
                        data-toggle="tooltip" data-placement="bottom" title="GitHub">
                        <i class="fa-brands fa-square-github fa-xl text-dark"></i>
                      </a>
                      
                    </div>
                    <div class="col-1">
                      <a href="https://www.google.com"  target="_blank" rel="noopener"
                        data-toggle="tooltip" data-placement="bottom" title="LinkedIn">
                        <i class="fa-brands fa-linkedin fa-xl text-dark"></i>
                      </a>
                      
                    </div>
                    <div class="col-1">
                      <a href="https://www.google.com"  target="_blank" rel="noopener"
                        data-toggle="tooltip" data-placement="bottom" title="Resume">
                        <i class="fa-solid fa-file fa-xl text-dark"></i>
                      </a>
                      
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- right area Input section -->
          <div class="col-7 pe-0">
            <div class="contact-form-box border rounded border-dark border-3 p-3 h-100"
            ref="contactFormBoxRef"
            :class="{ 'contact-form-box--visible': contactFormBoxVisible }"
            >
              <form class="d-flex flex-column h-100" action="https://formspree.io/f/xrezrkae" method="POST">
                <div class="form-group mb-2">
                  <label for="name">Name</label>
                  <input type="text" class="form-control border border-dark border-2" id="name" placeholder="Name" name="name"/>
                </div>
                <div class="form-group mb-2">
                  <label for="email">Email address</label>
                  <input type="email" class="form-control border border-dark border-2" id="email"
                    placeholder="name@example.com" name="email"/>
                </div>

                <div class="form-group mb-2">
                  <label for="subject">Subject</label>
                  <input type="text" class="form-control border border-dark border-2" id="subject"
                    placeholder="Subject" name="subject"/>
                </div>

                <div class="form-group">
                  <label for="message">Message</label>
                  <textarea class="form-control border border-dark border-2" id="message" rows="5" name="message" placeholder="Message"></textarea>
                </div>

                <button type="submit" class="btn btn-warning w-100 mt-auto border border-dark border-2">Send</button>
              </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.contact-container {
  background-color: var(--contact-section-background);
}

/* left side box */
.contact-details-box {
  background-color: var(--contact-details-background);
  box-shadow: 10px 12px var(--shadow-color);
  opacity: 0;
  transform: translateX(-40px);
}
.contact-details-box--visible.contact-details-box {
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

.contact-item:hover {
  box-shadow: 5px 5px;
  transform: scale(1.02);

}



/* right side box */
.contact-form-box {
  box-shadow: 10px 12px var(--shadow-color);
  background-color: var(--button-background);
  opacity: 0;
  transform: translateX(40px);
}
.contact-form-box--visible.contact-form-box {
   animation: slideInRight 0.8s ease-out forwards;
  animation-delay: 0.3s; 
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



.card-title {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 1.5em;
  font-weight: bold;

}

.card-text {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 1.1em;

}

h4 {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 1.5em;
}

p {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 1.1em;
}

.form-group {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 1.1em;
}

.btn {
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
  font-size: 1.1em;
}
.btn:hover {
  box-shadow: 5px 5px;
  transform: scale(1.015);
}
</style>
