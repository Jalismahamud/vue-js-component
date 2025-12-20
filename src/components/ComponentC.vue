<script setup>
 const props = defineProps(['course']);
</script>

<template>
     <p>Hello there i am component C</p>
     <input type="text" v-model="course.name">
     <input type="text" v-model="course.price">
</template>