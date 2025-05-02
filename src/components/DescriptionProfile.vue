<script setup>
import { defineProps } from 'vue'
const props = defineProps({
    name: String,
    description: String
})
</script>

<template>
    <div class="description-profile">
        <span class="label">{{ props.name }}</span>
        <span class="label">{{ props.description }}</span>
    </div>
</template>

<style scoped>
.description-profile {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border: 1px solid #000;
    padding-left: 1rem;
    padding-right: 1rem;
}

.label {
    color: #eee;
    margin: 5px 0;
}

.label:nth-of-type(1) {
    font-size: 1.25rem;
    font-weight: 700;
    line-height: 1.75rem;
}

.label:nth-of-type(2) {
    padding: 0 .5rem;
    text-align: center;
    font-size: .8rem;
    line-height: 1.25;
    font-weight: normal;
}
</style>