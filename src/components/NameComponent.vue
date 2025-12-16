<script setup>

    const props = defineProps([
        'fname' , 'lname'
    ]);

    const emit = defineEmits(['update:fname' , 'update:lname']);
</script>

<template>
    <p>
        <label for="">Frist Name</label>
        <input type="text" :value="fname" @input="$emit('update:fname', $event.target.value)">
    </p>
    <p>
        <label for="">Last Name</label>
        <input type="text" :value="lname" @input="$emit('update:lname' , $event.target.value)">
    </p>
</template>