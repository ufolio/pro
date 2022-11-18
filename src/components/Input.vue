<template>
    <label>
        <p>{{ text }}</p>
        <input 
            type="text" 
            name="" 
            value=""
            :placeholder="placeholder"
        >
    </label>
</template>

<script setup>
// import { defineComponent } from '@vue/composition-api'

const props = defineProps(['text', 'placeholder']);

</script>
