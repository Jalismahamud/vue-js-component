<script setup>
    import TestComponent  from './TestComponent.vue';
    const props = defineProps([
        'person'
    ]);
</script>

<template>
    <p>
        <TestComponent label="Name" v-model="person.name" /><br>
        <TestComponent label="Email" v-model="person.email" /> <br>
        <TestComponent label="Age" v-model="person.age" />
    </p>
</template>