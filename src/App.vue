<script setup>
import Navbar from "./components/Navbar.vue";
import HomeView from "./views/HomeView.vue";
</script>

<template>
    <div class="page">
        <div class="navbar">
             <Navbar />
        </div>
        <div class="main-container">
            <router-view></router-view>
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
    padding-left: 40px;
    padding-right: 40px;
}
</style>
