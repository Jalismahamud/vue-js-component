<script setup>
    const props = defineProps([
        'person'
    ]);
</script>

<template>
    <p>
        <label for="">Name</label><br>
        <input type="text" v-model="person.name"><br>
        <label for="">Email</label><br>
        <input type="text" v-model="person.email"><br>
        <label for="">Age</label><br>
        <input type="text" v-model="person.age"><br>
    </p>
</template>