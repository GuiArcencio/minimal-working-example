<script setup>
// Change the following initial value
// to ref(false) to reproduce the bug
const render = ref(true)
onMounted(() => {
    render.value = true
})
</script>

<template>
    <div v-if="render">
        <nuxt-img src="/red.png" width="250" height="250" alt="Image not shown."/>
    </div>
</template>