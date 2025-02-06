<script setup>
import { ref } from 'vue'
/* Ref: Used for primitive and non-premitive data types. everything is allowed here */

const count = ref(0)

const username = ref('')

const usersList = ref(['jai', 'gopi', 'raham'])

const employeeInfo = ref({ name: 'jai', age: 20, location: ['Guntur', 'Hyd'], isMarried: false })
</script>

<template>
  <h4>Count: {{ count }}</h4>
  <button v-on:click="count++">+</button>
  <button v-on:click="count--">-</button>

  <h4>Username : {{ username }}</h4>
  <button @click="username = 'jailadin'">Set Username</button>

  <h4>Users : {{ usersList }}</h4>
  <button @click="usersList.push('mahesh', 'raju')">Add Users</button>

  <h4>EmployeeInfo</h4>
  <h5>Employee Name : {{ employeeInfo.name }}</h5>
  <h5>Employee Age : {{ employeeInfo.age }}</h5>
  <h5>Employee Location : {{ employeeInfo.location }}</h5>
  <h5>Employee Married : {{ employeeInfo.isMarried }}</h5>

  <button @click="employeeInfo.name = 'Gopi'">Change Name</button>
  <button @click="employeeInfo.age = 30">Change Age</button>
  <button @click="employeeInfo.location.push('SAP')">Add Location</button>
  <button @click="employeeInfo.isMarried = true">Change Status</button>
</template>
