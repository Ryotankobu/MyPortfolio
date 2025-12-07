<script setup>
import SectionHeader from './common/SectionHeader.vue';

</script>

<template>
    <div id="experience" class="section-anchor"></div>
     <div class="experience-container d-flex flex-column py-5">
        <SectionHeader 
        title="What I experienced"
        description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas metus massa, imperdiet eu convallis eu, semper quis est. Pellentesque auctor pharetra lectus. Aenean cursus sem ante, eu elementum quam luctus ut. Nulla imperdiet semper justo sit amet rutrum. Vivamus."
    />
        <div class="experiencce-section-main container-fluid bg-primary flex-grow-1 p-0 d-flex flex-column">
            <div class="card work-experience-card mt-4">aa</div>
            <div class="card study-experience-card flex-grow-1 mt-4">aaa</div>

        </div>
    </div>
</template>

<style scoped>
.experience-container {
    height: 1500px;
    background-color: navy;
}
.work-experience-card {
    height: 800px;
}
</style>