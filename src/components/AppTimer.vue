<template>
    <div class="is-flex is-align-items-center is-justify-content-space-between">
        <AppChronometer :time="time" />

        <button class="button" @click="start" :disabled="timerIsActive">
            <span class="icon">
                <i class="fas fa-play"></i>
            </span>
            <span>Play</span>
        </button>

        <button class="button" @click="finish" :disabled="!timerIsActive">
            <span class="icon">
                <i class="fas fa-stop"></i>
            </span>
            <span>Stop</span>
        </button>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import AppChronometer from './AppChronometer.vue';

export default defineComponent({
    name: 'AppTimer',
    data() {
        return {
            time: 0,
            timer: 0,
            timerIsActive: false
        };
    },
    methods: {
        start() {
            this.timerIsActive = true;
            if (!this.timer) {
                this.timer = setInterval(() => {
                    this.time += 1;
                }, 1000);
            }
        },
        finish() {
            clearInterval(this.timer);
            this.timer = 0;
            this.timerIsActive = false;
        }
    },
    components: { AppChronometer }
})
</script>
