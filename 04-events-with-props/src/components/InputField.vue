<script setup>
import { ref } from 'vue';

    defineEmits(['update:modelValue']);

    defineProps({
        modelValue:{
            type: String,
            required:false,
            default:''
        },
        id: {
            type: String,
            required:true
        },
        placeholder:{
            type: String,
            default: '',
            required:true
        },
        label: {
            type: String,
            default: '',
            required:true
        }
    })
    const name = ref('')
</script>

<template>
    <label :for="id">{{ label }}</label>
    <input 
        :value="modelValue"
        :id="id"
        :type="type" 
        :placeholder="placeholder"
        @input="$emit('update:modelValue', $event.target.value)"/>

        
</template>


<style scoped>
</style>
