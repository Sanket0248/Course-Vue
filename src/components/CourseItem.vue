<template>
    <RoundedCard >

        <h3 class="p-4 text-xl font-medium border-b border-gray-200">{{title}}</h3>

        <p class="p-4  border-b border-gray-200">{{price}}</p>

        <p class="p-4 text-medium">{{description}}</p>
        <div class="flex justify-end p-4">
            <button 
                @click="$emit('click')"
                class="bg-blue-500 text-white px-4 py-2 rounded-md hover:bg-blue-600">Enroll Now</button>   
        </div>
    </RoundedCard>
</template>

<!--1. {{ }} — Displaying Data :The double curly braces are Vue's way of displaying data/variables in the template:
defineProps — Receiving Data from Parent :Props are how a parent component passes data down to a child component. defineProps tells Vue "this component expects these values from outside":
defineEmits + $emit — Sending Events to Parent :This is the opposite of props — it's how a child talks back to the parent.
-->
<script setup>
import RoundedCard from './RoundedCard.vue';

    defineProps({
        title: String,
        price: String,
        description: String
    })

    defineEmits(['click'])
</script>