<script setup>
import SectionHeader from "./common/SectionHeader.vue";
import sampleImage from "@/assets/images/bellsprout.png";
</script>

<template>
  <div id="contact" class="section-anchor"></div>
  <div class="contact-container">
    <div class="experience-container d-flex flex-column py-5 px-5">
      <SectionHeader
        title="Contact Me"
        description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas metus massa, imperdiet eu convallis eu, semper quis est. Pellentesque auctor pharetra lectus. Aenean cursus sem ante, eu elementum quam luctus ut. Nulla imperdiet semper justo sit amet rutrum. Vivamus."
      />
      <div class="contact-section-main container-fluid">
        <div class="row">
          <div class="col-5 ps-0">
            <div
              class="card contact-details-box border rounded border-3 border-dark p-3 d-flex flex-column justify-content-between"
            >
              <div class="contact-explanation-area w-100">
                <h3 class="card-title">aaaaaa</h3>
                <p class="card-text">
                  aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
                </p>
              </div>
              <div class="contact-items-area mt-3">
                <!-- contact item1 -->
                <div class="contact-item border border-dark border-2 rounded mb-2">
                  <div class="row p-2">
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
                      class="col-10 p-0 d-flex flex-column justify-content-between ps-2"
                    >
                      <h4 class="m-0">Email</h4>
                      <p class="m-0">ucp4fya7@yahoo.co.jp</p>
                    </div>
                  </div>
                </div>

                <!-- contact item2 -->
                <div class="contact-item border border-dark border-2 rounded mb-2">
                  <div class="row p-2">
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
                      class="col-10 p-0 d-flex flex-column justify-content-between ps-2"
                    >
                      <h4 class="m-0">Email</h4>
                      <p class="m-0">ucp4fya7@yahoo.co.jp</p>
                    </div>
                  </div>
                </div>

                <!-- contact item3  -->
                <div class="contact-item border border-dark border-2 rounded mb-2">
                  <div class="row p-2 ">
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
                      class="col-10 p-0 d-flex flex-column justify-content-between ps-2"
                    >
                      <h4 class="m-0">Email</h4>
                      <p class="m-0">ucp4fya7@yahoo.co.jp</p>
                    </div>
                  </div>
                </div>
              </div>
              <div class="contact-icons-area d-flex flex-column p-2">
                <p class="m-0 mb-1">aaaaaaaaaaaaaaaaaaaaaa</p>
                <div class="icon-box">
                  <div class="row">
                    <div class="col-2">
                      <img
                        :src="sampleImage"
                        class="card-img-top w-75"
                        alt="..."
                      />
                    </div>
                    <div class="col-2">
                      <img
                        :src="sampleImage"
                        class="card-img-top w-75"
                        alt="..."
                      />
                    </div>
                    <div class="col-2">
                      <img
                        :src="sampleImage"
                        class="card-img-top w-75"
                        alt="..."
                      />
                    </div>
                    <div class="col-2">
                      <img
                        :src="sampleImage"
                        class="card-img-top w-75"
                        alt="..."
                      />
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Input section -->
          <div class="col-7 pe-0">
            <div class="contact-form-box border rounded border-dark border-3 p-3 h-100">
              <form class="d-flex flex-column h-100">
                <div class="form-group mb-2">
                  <label for="name">Name</label>
                  <input
                    type="text"
                    class="form-control border border-dark border-2"
                    id="name"
                    placeholder="Name"
                  />
                </div>
                <div class="form-group mb-2">
                  <label for="email">Email address</label>
                  <input
                    type="email"
                    class="form-control border border-dark border-2"
                    id="email"
                    placeholder="name@example.com"
                  />
                </div>

                <div class="form-group mb-4">
                  <label for="subject">Subject</label>
                  <input
                    type="text"
                    class="form-control border border-dark border-2"
                    id="subject"
                    placeholder="Subject"
                  />
                </div>
               
                <div class="form-group">
                  <label for="message"
                    >Message</label
                  >
                  <textarea
                    class="form-control border border-dark border-2"
                    id="message"
                    rows="5"
                  ></textarea>
                </div>

                <button type="submit" class="btn btn-warning w-100 mt-auto border border-dark border-2">Sign in</button>
              </form>
            </div>
          </div>
        </div>
      </div>
      <!-- <div class="experiencce-section-main container-fluid bg-primary flex-grow-1 p-0 d-flex flex-column">
            <div class="card work-experience-card mt-4">aa</div>
            <div class="card study-experience-card flex-grow-1 mt-4">aaa</div>

        </div> -->
    </div>
  </div>
</template>

<style scoped>
.contact-container {
  background-color: var(--contact-section-background);
}
.contact-details-box {
  background-color: var(--contact-details-background);
  box-shadow: 10px 12px  var(--shadow-color);
 
}
.contact-form-box {
  box-shadow: 10px 12px  var(--shadow-color);
  
   background-color: var( --button-background);
 
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
</style>
