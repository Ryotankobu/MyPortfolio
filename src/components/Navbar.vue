<script setup>
import { RouterLink, useRoute } from 'vue-router';
const props = defineProps({
  currentSection: {
    type: String,
    default: 'hero'
  }
})
</script>

<template>
  <nav class="navbar navbar-expand-lg bg-body-tertiary">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">
        <h2>My Portfolio</h2>
      </a>
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
        <ul class="navbar-nav gap-3">
          <li class="nav-item border rounded-4 px-2">
            <RouterLink 
              class="nav-link" 
              :class="{active: props.currentSection === 'about'}"
              :to="{name: 'homeView', hash: '#about'}">
              ABOUT
            </RouterLink>
          </li>
          <li class="nav-item border rounded-4 px-2">
            <RouterLink 
              class="nav-link" 
              :class="{active: props.currentSection === 'experience'}"
              :to="{name: 'homeView', hash: '#experience'}">
              EXPERIENCE
            </RouterLink>
          </li>
          <li class="nav-item  border rounded-4 px-2">
            <RouterLink 
              class="nav-link" 
              :class="{active: props.currentSection === 'project'}"
              :to="{name: 'homeView', hash: '#project'}">
              PROJECT
            </RouterLink>
          </li>
          <li class="nav-item  border rounded-4 px-2">
            <RouterLink 
              class="nav-link" 
              :class="{active: props.currentSection === 'contact'}"
              :to="{name: 'homeView', hash: '#contact'}">
              CONTACT
            </RouterLink>
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
.nav-link.active {
  font-weight: bold;
  text-decoration: underline;
}
.nav-item {
  
}
</style>
