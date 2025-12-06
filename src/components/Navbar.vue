<script setup>
import { RouterLink, useRoute } from 'vue-router';
</script>

<template>
  <nav class="navbar navbar-expand-lg bg-body-tertiary">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">My Portfolio</a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <RouterLink class="nav-link" :to="{name: 'homeView', hash: '#about'}">ABOUT</RouterLink>
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link" :to="{name: 'homeView', hash: '#experience'}">EXPERIENCE</RouterLink>
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link" :to="{name: 'homeView', hash: '#project'}">PROJECT</RouterLink>
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link" :to="{name: 'homeView', hash: '#contact'}">CONTACT</RouterLink>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  padding-left: 40px;
  padding-right: 40px;
}
.navbar-collapse {
  background-color: var(--bs-tertiary-bg) !important;
}
.container-fluid {
  padding: 0;
}
</style>
