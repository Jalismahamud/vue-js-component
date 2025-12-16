<script setup>
defineProps(["label", "modelValue"]);
defineEmits(["update:modelValue"]);
</script>

<template>
  <div>
    <label>{{ label }}</label><br />
    <input
      type="text"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
    />
  </div>
</template>
