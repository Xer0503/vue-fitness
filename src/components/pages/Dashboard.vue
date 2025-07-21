<script setup>
    import { gymHealthFacts } from '../../utils'
    const randNumber = Math.floor(Math.random() * gymHealthFacts.length)
    const todayFact = gymHealthFacts[randNumber]
    import Program from '../Program.vue'
</script>

<template>
    <section class="h-full flex flex-col justify-items-center justify-center px-5">
        <!--Card-->
        <div class="my-5 border shadow-md rounded  w-full md:w-1/2 mx-auto px-5 py-5 space-y-5">
            <h1 class="font-semibold text-5xl">Welcome Skinny Boy!</h1>
            <p class="font-bold text-md text-orange-600">Daily Tips</p>
            <p class="font font-medium text-2xl text-center">"{{ todayFact }}"</p>
            <div class="text-center">
                <button class="text-[18px] px-5 py-2 text-dark shadow rounded border-1 border-orange-600 hover:bg-orange-600 hover:text-white">Start Workout</button>
            </div>
        </div>
        <!--End of Card-->
    </section>
    <Program />
</template>
<style scoped>
</style>