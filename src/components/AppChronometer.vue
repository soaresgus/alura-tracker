<template>
    <section>
        <strong>
            {{ formattedTime }}
        </strong>
    </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: 'AppChronometer',
    props: {
        time: {
            type: Number,
            required: true,

        }
    },
    computed: {
        formattedTime(): string {
            return new Date(this.time * 1000).toISOString().substr(11, 8)
        }
    },
})
</script>
