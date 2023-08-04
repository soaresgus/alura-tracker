<template>
    <div class="box">
        <div class="columns">
            <div class="column is-8" role="form">
                <input type="text" class="input" placeholder="Qual tarefas você deseja iniciar">
            </div>

            <div class="column">
                <AppTimer />
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import AppTimer from './AppTimer.vue';

export default defineComponent({
    name: "AppForm",
    components: { AppTimer }
})
</script>
