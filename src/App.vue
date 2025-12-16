<script setup>
import { reactive, ref } from 'vue'
import TestComponent from './components/TestComponent.vue';
import PersonComponent from './components/PersonComponent.vue';

const name = ref('Jalis Mahamud')
const email = ref('jon@gmail.com')

const person = reactive({
  name: 'jalis Mahamud',
  email: 'jalis@mahamud.com',
  age: 25
});
</script>

<template>
  <div>
    <p>Name: {{ person.name }}</p>
    <p>Email: {{ person.email }}</p>
    <p>Age: {{ person.age }}</p>
  </div>

 <div>
   <PersonComponent :person="person" />
 </div>
 
</template>
