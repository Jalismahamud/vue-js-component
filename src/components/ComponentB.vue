<script setup>
    import ComponentC  from './ComponentC.vue';
    import { inject } from 'vue';


    const course = inject('course')

    // const props = defineProps(['course']);
</script>

<template>

    <p>jalis {{  course.name }}</p>
    <p> {{ course.price }}</p>

    <ComponentC :course="course" />
</template>