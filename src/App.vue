<template>
  <div class="p-4 space-y-8">
    <h1 class="text-4xl font-medium">Course Hub</h1>
    
    <h2 class="text-2xl font-medium">All Courses</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mb-8">
      <CourseItem 
      v-for="i in 3" 
      :key="i"
      :title="`Course ${i}`"
      :price="`$${i * 10}`"
      :description="`This is the description for course ${i}`"
      @click="alert(`You clicked on course ${i}`)">
    </CourseItem> 
    <!--rendering the course item component 3 times to display 3 courses 
      The : is shorthand for v-bind:. It tells Vue "treat this value as JavaScript, not plain text".
      @click is shorthand for v-on:click — it's Vue's way of listening to events. When the component is clicked, it runs whatever you pass to it.
    -->
    </div>


    <h2 class="text-2xl font-medium">Your Courses</h2>
  </div>
</template>


<script setup>
import CourseItem from './components/CourseItem.vue'//importing the course item component to be used in the template
</script>