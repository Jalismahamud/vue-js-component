<script setup>
    import ComponentB from './ComponentB.vue';
    const props = defineProps(
        ['course']
    );
</script>

<template>
    <p>
        Course Name in Component B{{ course.name }}
    </p>
    <p>
        <ComponentB :course="course" />
    </p>
</template>