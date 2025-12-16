<script setup>

    const props = defineProps([
        'label' , 'modelValue'
    ]);
    
    const emit = defineEmits('update:modelValue')
</script>

<template>
    <p>
        <label for="">{{ label }}</label>
        <input type="checkbox" class="ml-5" :checked="modelValue" @change="$emit('update:modelValue' , $event.target.checked)">
        <!-- <input type="checkbox" class="ml-5" :checked="modelValue" @change="$emit('update:modelValue' , !modelValue)"> -->
    </p>
</template>