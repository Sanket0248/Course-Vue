<template>
  
    <h1 class="text-4xl font-medium">Course Hub</h1>
    
    <h2 class="text-2xl font-medium">All Courses</h2>
    <CourseItem v-for="i in 4" key="i"></CourseItem>

    <h2 class="text-2xl font-medium">Your Courses</h2>

</template>


<script setup>
import CourseItem from './components/CourseItem.vue'
</script>