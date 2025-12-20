<script setup>
    import ComponentB from './ComponentB.vue';
    // const props = defineProps(
    //     ['course']
    // );
    import {provide} from 'vue';

    import {inject} from 'vue';

    provide('course', course)

    const course = inject('course')
</script>

<template>
    <p>
        Course Name in Component B {{ course.name }}
        <span>Test : {{ course.price }}</span>
    </p>
    <p>
        <ComponentB/>
    </p>
</template>