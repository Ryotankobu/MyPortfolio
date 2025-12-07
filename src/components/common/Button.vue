<script setup>
    defineProps({
        title: String
    })

</script>

<template>
    <button type="button" class="btn btn-primary w-100">{{ title }}</button>
</template>

<style scoped>
</style>