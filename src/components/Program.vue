<script setup>
    import { workoutProgram } from '../utils';
    import { selectWorkout } from '../utils/displayState';
    import Push from '../assets/push-up.png'
    import Squat from '../assets/squats.png'
    import Pull from '../assets/lighting.png'
    const workoutTypes = ['Push', 'Pull', 'Legs'];
</script>

<template>
    <section class="grid grid-cols-2 md:grid-cols-3 px-10 py-5 gap-6">
        <div
        :key="workoutId" v-for="(workout, workoutIdx) in Object.keys(workoutProgram)" 
        class="gap-py-5 p-3"
        >
            <div @click="selectWorkout = workoutIdx+1" class="rounded-3xl border-1 shadow p-5 hover:bg-orange-400 hover:text-white hover:shadow-2xl active:bg-orange-400 active:text-white">
                <p class="font-semibold">Day {{ workoutIdx < 9 ? '0' + (workoutIdx + 1) : workoutIdx + 1 }}</p>
                <div v-if="workoutIdx % 3 === 0">
                    <img :src="Push" alt="Company Logo" loading="lazy" class="mx-auto w-15" />
                </div>
                <div v-if="workoutIdx % 3 === 1">
                    <img :src="Pull" alt="Company Logo" loading="lazy" class="mx-auto w-15" />
                </div>
                <div v-if="workoutIdx % 3 === 2">
                    <img :src="Squat" alt="Company Logo" loading="lazy" class="mx-auto w-15" />
                </div>
                <h3 class="font-bold text-2xl text-center">{{ workoutTypes[workoutIdx % 3] }}</h3>
            </div>
        </div>
    </section>
</template>

<style scoped>
</style>