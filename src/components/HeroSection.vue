<script setup>
  import Button from './common/Button.vue';
  import sampleImage from '@/assets/images/bellsprout.png';
</script>

<template>
  <div class="hero-container container-fluid py-5 px-5">
    <div class="row d-flex align-items-stretch">
      <div
        class="col-7 px-0 pe-2 d-flex"
        style="background-color: pink"
      >
        <div class="card w-100 h-100">
          <div class="card-body p-4 d-flex flex-column">
            <h3 class="card-title mb-0">Lorem ipsum dolor sit.</h3>
            <!-- <h6 class="card-subtitle mb-2 text-body-secondary">
              Card subtitle
            </h6> -->
            <h1 class="display-1 bold fw-bold">Ryota Ando</h1>
            <h3 class="card-title mt-3">Lorem ipsum dolor sit.</h3>
            <p class="card-text">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas metus massa, imperdiet eu convallis eu, semper quis est. Pellentesque auctor pharetra lectus. Aenean cursus sem ante, eu elementum quam luctus ut. Nulla imperdiet semper justo sit amet rutrum. Vivamus placerat orci eu ligula tincidunt, id facilisis justo pharetra. Donec ornare enim sed libero scelerisque pulvinar. Quisque elementum lacus eget felis ullamcorper rhoncus. Donec condimentum porttitor tristique. Pellentesque eleifend vitae nulla vel interdum. Integer dui.Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas metus massa, imperdiet eu convallis eu, semper quis est. Pellentesque auctor pharetra lectus. Aenean cursus sem ante, eu elementum quam luctus ut. Nulla imperdiet semper justo sit amet rutrum. Vivamus placerat orci eu ligula tincidunt, id facilisis justo pharetra. Donec ornare enim sed libero scelerisque pulvinar. Quisque elementum lacus eget felis ullamcorper rhoncus. Donec condimentum porttitor tristique. Pellentesque eleifend vitae nulla vel interdum. Integer dui.
            </p>
            <div class="row mt-auto">
              <div class="col-6">
                <Button title="test"/>
              </div>
              <div class="col-6">
                <Button title="test"/>
              </div>
            </div>
         
          </div>
        </div>
      </div>
      <div class="col-5 px-0 ps-2 d-flex" style="background-color: plum">
        <div class="card w-100 h-100">
          
          <div class="card-body p-4 d-flex flex-column">
            <img :src="sampleImage" class="card-img-top w-100 hero-image mx-auto d-block" alt="..." />
            <div class="border rounded mt-2 mb-4">
              <p>section1</p>
            </div>
            <div class="border rounded">
              <p>section2</p>
            </div>
          
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.hero-container {
  
  background-color: green;
}
.hero-image {
  width: 100%;
  height: 100%;
  object-fit: cover; 
}
</style>
