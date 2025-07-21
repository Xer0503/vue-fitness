<script setup>
    import Nav from './Nav.vue'
    import Welcome from '../pages/Welcome.vue'
    import Dashboard from '../pages/Dashboard.vue'
    import Workout from '../pages/Workout.vue'
    import Footer from './Footer.vue'
    import { selectDisplay } from '../../utils/displayState'
</script>

<template>
    <header>
        <Nav />
    </header>
    <main>
        <!-- PAGE 1 -->
        <Welcome v-if="selectDisplay == 1" />
        <!-- PAGE 2 -->
        <Dashboard v-if="selectDisplay == 2" />  
        <!-- PAGE 3 -->
        <Workout v-if="selectDisplay == 3" />
    </main>
    <footer>
        <Footer />
    </footer>
</template>

<style scoped>
</style>