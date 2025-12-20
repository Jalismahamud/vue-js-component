<script setup>
    // import ComponentC  from './ComponentC.vue';
    // import { inject } from 'vue';


    // const course = inject('course')

    import {course} from '../data/data.js';

    // const props = defineProps(['course']);
</script>

<template>

    <p>jalis {{  course.name }}</p><br>
    <p> {{ course.isActive }}</p>

    <ComponentC :course="course" />
</template>