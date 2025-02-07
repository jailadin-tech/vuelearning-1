<script setup>
import { ref } from 'vue'

const name = ref('')
const email = ref('')
const phone = ref('')
</script>

<template>
  <form @submit.prevent="$emit('userRegister', name, email, phone)">
    <input type="text" placeholder="name" name="username" v-model="name" />
    <input type="text" placeholder="email" name="emailId" v-model="email" />
    <input type="text" placeholder="phone" name="phoneno" v-model="phone" />
    <button type="submit">submit</button>
  </form>
</template>
