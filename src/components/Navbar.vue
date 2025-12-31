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
  <nav class="navbar navbar-expand-lg navbar-background">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">
        <h2 style="color: var(--navbar-text)">My Portfolio</h2>
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
          <li class="nav-item border px-2" :class="{active: props.currentSection === 'about'}">
            <RouterLink 
              class="nav-link" 
              :class="{active: props.currentSection === 'about'}"
              :to="{name: 'homeView', hash: '#about'}"
              style="color: var(--navbar-text)">
              
              ABOUT
            </RouterLink>
          </li>
          <li class="nav-item border px-2" :class="{active: props.currentSection === 'experience'}">
            <RouterLink 
              class="nav-link" 
              :class="{active: props.currentSection === 'experience'}"
              :to="{name: 'homeView', hash: '#experience'}"
              style="color: var(--navbar-text)">
              EXPERIENCE
            </RouterLink>
          </li>
          <li class="nav-item  border px-2" :class="{active: props.currentSection === 'project'}">
            <RouterLink 
              class="nav-link" 
              :class="{active: props.currentSection === 'project'}"
              :to="{name: 'homeView', hash: '#project'}"
              style="color: var(--navbar-text)">
              PROJECT
            </RouterLink>
          </li>
          <li class="nav-item  border px-2" :class="{active: props.currentSection === 'contact'}">
            <RouterLink 
              class="nav-link" 
              :class="{active: props.currentSection === 'contact'}"
              :to="{name: 'homeView', hash: '#contact'}"
              style="color: var(--navbar-text)">
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
.navbar-background {
  background-color: var(--navbar-background);
}
.navbar-collapse {
  background-color: var(--navbar-background) !important;
}
.container-fluid {
  padding: 0;
  
}
.nav-link.active {
  font-weight: bold;
  text-decoration: underline;
}
.nav-item {
  font-family: "Press Start 2P", system-ui;
  font-weight: 400;
  font-style: normal;
  border-radius: 50% 10% 50% 10% / 10% 50% 10% 50%;
}
.nav-item.active {
  transform: rotate(4deg);
  scale: (1.2);
  background-color: var(--navbar-button-active);

}
h2 {
  font-family: "Press Start 2P", system-ui;
  font-weight: 400;
  font-style: normal;
}
@media (max-width: 576px) {
  h2 {
    font-size: 1rem;
  }
  .navbar-nav {
    padding: 10px;

  }
  .nav-item {
  font-weight: 200;
  font-size: 1rem;
  }
  .nav-item.active {
  transform: rotate(2deg);
}
}
@media (max-width: 1100px) {
  .nav-item {
  font-weight: 200;
  font-size: 0.8rem;
  margin: 5px;
  }
  .nav-item.active {
  transform: rotate(2deg);
}
.navbar-collapse  {
  margin-top: 20px;
}
}
</style>
