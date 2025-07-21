<script setup>
    import { workoutProgram } from '../utils';
    const workoutTypes = ['Push', 'Pull', 'Legs']
</script>

<template>
    <section class="grid grid-cols-2 md:grid-cols-3 px-10 py-5 gap-5">
        <div
        :key="workoutId" v-for="(workout, workoutIdx) in Object.keys(workoutProgram)" 
        class="gap-py-5 rounded-3xl border-1 shadow-2xl p-3 hover:bg-orange-600 hover:text-white hover:shadow-2xl"
        >
            <p class="font-semibold">Day {{ workoutIdx < 9 ? '0' + (workoutIdx + 1) : workoutIdx + 1 }}</p>
            ICON
            <h3>Types</h3>
        </div>
    </section>
</template>

<style scoped>
</style>