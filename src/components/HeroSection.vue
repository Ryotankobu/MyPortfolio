<script setup></script>

<template>
  <div class="hero-container container-fluid">
    <div class="row d-flex h-100">
      <div
        class="col-7 h-100 pt-4 pb-4 px-0 pe-2"
        style="background-color: pink"
      >
        <div class="card w-100 h-100" style="width: 18rem">
          <div class="card-body">
            <h5 class="card-title">Card title</h5>
            <h6 class="card-subtitle mb-2 text-body-secondary">
              Card subtitle
            </h6>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card’s content.
            </p>
            <a href="#" class="card-link">Card link</a>
            <a href="#" class="card-link">Another link</a>
          </div>
        </div>
      </div>
      <div class="col-5 pt-4 pb-4 px-0 ps-2" style="background-color: plum">
        <div class="card w-100 h-100">
          <img src="..." class="card-img-top" alt="..." />
          <div class="card-body">
            <h5 class="card-title">Card title</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card’s content.
            </p>
            <a href="#" class="btn btn-primary">Go somewhere</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.hero-container {
  height: 500px;
  background-color: green;
}
</style>
