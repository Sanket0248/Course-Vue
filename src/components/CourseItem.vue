<template>
    <div class="bg-white border border-grey-200 rounded-md">

        <h3 class="p-4 text-xl font-medium border-b border-gray-200">{{title}}</h3>

        <p class="p-4  border-b border-gray-200">{{price}}</p>

        <p class="p-4 text-medium">{{description}}</p>
        <div class="flex justify-end p-4">
            <button 
                @click="$emit('click')"
                class="bg-blue-500 text-white px-4 py-2 rounded-md hover:bg-blue-600">Enroll Now</button>   
        </div>
    </div>
</template>

<script setup>
    defineProps({
        title: String,
        price: String,
        description: String
    })

    defineEmits(['click'])
</script>