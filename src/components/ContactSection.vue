<script setup>
import SectionHeader from './common/SectionHeader.vue';
</script>

<template>
    <div id="contact" class="section-anchor"></div>
    <div class="contact-container">
        <div class="experience-container d-flex flex-column py-5 px-5">
        <SectionHeader 
        title="Contact Me"
        description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas metus massa, imperdiet eu convallis eu, semper quis est. Pellentesque auctor pharetra lectus. Aenean cursus sem ante, eu elementum quam luctus ut. Nulla imperdiet semper justo sit amet rutrum. Vivamus."
    />
        <div class="contact-section-main container-fluid bg-primary py-5">
            <div class="row">
                <div class="col-5 ps-0">
                    <div class="contact-details-box border rounded ">
                          
                    </div>
                    
                </div>
                <div class="col-7 pe-0">
                    <div class="contact-form-box border rounded">
                          
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
    background-color: peru;
}
.contact-details-box {
    height: 500px;
}
.contact-form-box {
    height: 500px;
}
</style>