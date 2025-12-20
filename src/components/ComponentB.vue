<script setup>
    import ComponentC  from './ComponentC.vue';

    const props = defineProps(['course']);
</script>

<template>

    <p>This is component B: {{  course.name }}</p>
    <p>Course price: {{ course.price }}</p>

    <ComponentC :course="course" />
</template>