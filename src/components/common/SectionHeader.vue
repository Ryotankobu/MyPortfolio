<script setup>
    defineProps({
        title: String,
        description: String,
    })

</script>

<template>
    <div class="section-header text-center bg-warning col-10 offset-1 pt-4 pb-4">
        <h1 class="pb-3">{{ title }}</h1>
        <p>{{ description }}</p>
    </div>

</template>

<style scoped>
</style>