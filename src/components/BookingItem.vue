<!-- This file represents a booked item component for displaying enrolled courses -->
<template>
    <CardSection>
        <template #body>
            <div class="flex justify-between items-center">
                <div>Vue Course</div>
                <RoundedButton>Go to Course</RoundedButton>
            </div>
        </template>
    </CardSection>
</template>

<script setup>
import CardSection from '@/components/CardSection.vue'
import RoundedButton from '@/components/RoundedButton.vue'
</script>
