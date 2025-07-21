<script setup>
    import { workoutProgram } from '../utils';
    const workoutTypes = ['Push', 'Pull', 'Legs']
</script>

<template>
    <section class="grid grid-cols-3 md:grid-cols-5 px-10 py-5 gap-5">
        <div
        :key="workoutId" v-for="(workout, workoutIdx) in Object.keys(workoutProgram)" 
        class="border gap-5 rounded shadow p-3"
        >
            <p>Day {{ workoutIdx < 9 ? '0' + (workoutIdx + 1) : workoutIdx + 1 }}</p>
            ICON
            <h3>Types</h3>
        </div>
    </section>
</template>

<style scoped>
</style>