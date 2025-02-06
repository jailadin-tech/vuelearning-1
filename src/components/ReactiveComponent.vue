<script setup>
import { reactive } from 'vue'

/* Reactive:   Work for non-premitive data types only not for single number */
const intialState = reactive({ vlu: { count: 0 }, users: ['jai', 'gopi'] })

const changeUser = () => {
  intialState.users[0] = 'Venkat'
  intialState.users[1] = 'Mahesh'
}
</script>
<template>
  <h4>Count: {{ intialState.vlu.count }}</h4>
  <button v-on:click="intialState.vlu.count++">+</button>
  <button v-on:click="intialState.vlu.count--">-</button>
  <p>Users: {{ intialState.users }}</p>

  <button @click="changeUser">Change User</button>
  <button @click="intialState.users.push('Raju')">Add User</button>
</template>
