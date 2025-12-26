<script setup>
import { onMounted } from 'vue'
import AboutSection from '@/components/AboutSection.vue';
import ContactSection from '@/components/ContactSection.vue';
import ExperienceSection from '@/components/ExperienceSection.vue';
import FooterSection from '@/components/FooterSection.vue';
import HeroSection from '@/components/HeroSection.vue';
import ProjectSection from '@/components/ProjectSection.vue';
import TextMarquee from '../components/common/TextMarquee.vue'
import TextMarqueeSlow from '@/components/common/TextMarqueeSlow.vue';


const emit = defineEmits(['sectionChange'])

const sectionIds = ['hero', 'about', 'experience', 'project', 'contact']

onMounted(() => {
    const observer = new IntersectionObserver(
        (entries) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    emit('sectionChange', entry.target.id)
                }
            })
        },
        {
            threshold: 0.5,
        }
    )

    sectionIds.forEach((id) => {
        const el=document.getElementById(id)
        if (el) {
            observer.observe(el)
        }
    })
})
</script>

<template>
    <HeroSection />
    <TextMarquee 
    text="Studied full‑time, worked nights, stayed focused. No shortcuts."
    :duration="20"/>
    <AboutSection />
    <TextMarqueeSlow text="RYOTA ANDO" />
    <ExperienceSection />
    <TextMarquee 
    text="I’ve taken the long road, and it made my work better."
    :duration="20"/>
    <ProjectSection />
    <ContactSection />
    <FooterSection />
</template>

<style scoped>
</style>