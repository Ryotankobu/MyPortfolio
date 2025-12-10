<script setup>
import Navbar from "./components/Navbar.vue";
import HomeView from "./views/HomeView.vue";
import { ref } from "vue";

const currentSection = ref('here')
const handleSectionChange = (section) => {
    currentSection.value = section
}
</script>

<template>
    <div class="page">
        <div class="navbar">
             <Navbar :currentSection="currentSection"/>
        </div>
        <div class="main-container">
            <router-view v-slot="{Component}">
                <component :is="Component" @section-change="handleSectionChange" />
            </router-view>
        </div>
    </div>
    

</template>

<style scoped>
.navbar {
    position: fixed;
    top: 0;
    left: 0;
    height: 80px;
    width: 100%;
    z-index: 1000;
}
.main-container {
    margin-top: 80px;
    background-color: red;
    width: 100%;
    box-sizing: border-box;
    /* padding-left: 40px;
    padding-right: 40px; */
}
</style>
