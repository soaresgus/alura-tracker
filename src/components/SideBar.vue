<template>
    <header>
        <h1>
            <img src="../assets/logo.svg">
        </h1>
    </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: 'SideBar',
})
</script>

<style scoped>
header {
    display: flex;
    justify-content: center;
    background: #0d3b66;
    padding: 1rem;
    width: 100%;
    height: 100vh;
}

img {
    widows: 120px;
    height: 120px;
}

@media (max-width: 768px) {
    header {
        padding: 2.5rem;
        height: auto;
    }
}
</style>
