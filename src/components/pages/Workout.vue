<script setup>
    import { selectWorkout } from '../../utils/displayState';
</script>

<template>
    <div class="h-fit">
        <!--Card-->
        <div class="flex justify-center items-center rounded-2xl shadow w-1/2 mx-auto my-10 py-5">
            <!--Head Card-->
            <div class="text-md font-bold">
                <p>Day {{ selectWorkout < 9 ? '0' + selectWorkout : selectWorkout }}</p>
            </div>
            <!--Body-->
        </div>
    </div> 
</template>

<style scoped>
</style>