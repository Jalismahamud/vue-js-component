<script setup>
import { reactive, ref, provide } from 'vue'
import TestComponent from './components/TestComponent.vue';
import PersonComponent from './components/PersonComponent.vue';
import NameComponent from './components/NameComponent.vue';
import CheckboxComponent from './components/CheckboxComponent.vue';
import ComponentA from './components/ComponentA.vue';
import {course} from './data/data.js';
import Button from './components/Button.vue';

const name = ref('Jalis Mahamud')
const email = ref('jon@gmail.com')

const person = reactive({
  name: 'jalis Mahamud',
  email: 'jalis@mahamud.com',
  age: 25
});



provide('course' , course);
const taskStatus = ref(true);
const fname = ref('Jalis');
const lname = ref('Mahamud');
</script>

<template>

  <div class="text-center">
    <label for="">Components Example</label>
    <p>
      <Button>
        <i><b></b></i>
      </Button>
    
    </p>
  </div>


 <!-- <p>This is app.vue . {{ course.duration }}</p>
 <componentA /> -->

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
