<script setup>
import { ref } from 'vue'
import TestComponent from './components/TestComponent.vue'

const name = ref('Jalis Mahamud')
const email = ref('jon@gmail.com')
</script>

<template>
  <div>
    <p>Name: {{ name }}</p>
    <p>Email: {{ email }}</p>
  </div>

  <TestComponent label="Name" v-model="name" />
  <TestComponent label="Email" v-model="email" />
</template>
