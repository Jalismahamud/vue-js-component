<script setup>
    import ComponentB from './ComponentB.vue';
import {course} from '../data/data.js';
    // const props = defineProps(
    //     ['course']
    // );
    import {provide} from 'vue';

    import {inject} from 'vue';

    // provide('course', course)

    // const course = inject('course')
</script>

<template>
    <!-- <p>
        Course Name in Component B {{ course.name }}
        <span>Test : {{ course.price }}</span>
    </p> -->
    <h3>This is component A.. {{ course.name }}</h3>
    <p>
        <ComponentB/>
    </p>
</template>