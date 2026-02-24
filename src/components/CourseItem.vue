<!-- This component represents a course item in the course hub. here all the avilable course information is displayed -->
<template>
    <CardSection>
        <template #header>
            {{title}}
        </template>

        <template #body>
            <p>{{price}}</p>
        </template>

        <template #footer>
            <p>{{description}}</p>
            <div class="flex justify-end p-4">
                <RoundedButton @click="$emit('click')">Purchase</RoundedButton>
            </div>
        </template>

    </CardSection>
</template>

<!--1. {{ }} — Displaying Data :The double curly braces are Vue's way of displaying data/variables in the template:
defineProps — Receiving Data from Parent :Props are how a parent component passes data down to a child component. defineProps tells Vue "this component expects these values from outside":
defineEmits + $emit — Sending Events to Parent :This is the opposite of props — it's how a child talks back to the parent.
-->
<script setup>
import CardSection from '@/components/CardSection.vue'
import RoundedButton from '@/components/RoundedButton.vue'

    defineProps({
        title: String,
        price: String,
        description: String
    })

    defineEmits(['click'])
</script>