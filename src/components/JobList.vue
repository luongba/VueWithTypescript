<template>
    <div v-for="job in jobs" :key="job.id">
        <ul>
            <li>
                {{ job.title }}
            </li>
            <li>
                {{ job.salary }}
            </li>
            <li>
                {{ job.location }}
            </li>
        </ul>
    </div>
</template>
<script lang="ts">
import type Job from '../types/Job';
import { defineComponent } from 'vue'
import type { PropType } from 'vue';
export default defineComponent({
    props: {
        jobs: {
            required: true,
            type: Array as PropType<Job[]>
        }
    }
})
</script>