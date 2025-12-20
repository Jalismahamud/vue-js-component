<script setup>
import { reactive, ref } from 'vue'
import TestComponent from './components/TestComponent.vue';
import PersonComponent from './components/PersonComponent.vue';
import NameComponent from './components/NameComponent.vue';
import CheckboxComponent from './components/CheckboxComponent.vue';
import ComponentA from './components/ComponentA.vue';


const name = ref('Jalis Mahamud')
const email = ref('jon@gmail.com')

const person = reactive({
  name: 'jalis Mahamud',
  email: 'jalis@mahamud.com',
  age: 25
});

const course = reactive({
  name: 'Vue 3 Course',
  price: 4333
})
const taskStatus = ref(true);
const fname = ref('Jalis');
const lname = ref('Mahamud');
</script>

<template>

 <p>This is App.vue file . {{ course.name }}</p>
  <componentA :course="course" />

 <!-- <div>
  <p class="pb-4 text-green-400">Orgining Taks Status: {{  taskStatus }}</p>
  <CheckboxComponent v-model="taskStatus" />

 </div>


  <div class="text-2xl text-green-600">
      Original Frist Name: {{ fname }} <br>
      Original Last Name: {{ lname }}
  </div>
  <div>
    <p>Name: {{ person.name }}</p>
    <p>Email: {{ person.email }}</p>
    <p>Age: {{ person.age }}</p>
  </div>

  <div>
    <i class="fas fa-solar-panel    ">Component</i>
    <p>
      <NameComponent v-model:fname="fname" v-model:lname="lname" />
    </p>
  </div>

 <div>
   <PersonComponent :person="person" />
 </div> -->
 
</template>
