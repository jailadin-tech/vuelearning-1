<script setup>
import { ref } from 'vue'
const price = ref(80)
const password = ref('mypassword')
const isActive = ref(true)

const isVisible = ref(true)

const isLogged = ref(true)
const username = 'jailadin'
const showdetails = ref(isLogged)
</script>
<template>
  <h4 v-if="price > 100">Too Costly</h4>
  <h4 v-else-if="price < 100">Reasonable Cost</h4>
  <h4 v-else>Price not mentioned</h4>

  <h4 v-if="password.length > 8">Strong Password</h4>
  <h4 v-else-if="password.length < 8">Weak Password</h4>
  <h4 v-else>password not mentioned</h4>

  <h4 v-if="isActive">This will show if it is true</h4>
  <h4 v-else>This will show if it is false</h4>

  <p v-show="isVisible">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem tempore eaque commodi magni vero
    quia in incidunt iste, dicta consequatur veniam dolorum nesciunt mollitia beatae ad sit ea,
    molestias ratione!
  </p>
  <button @click="isVisible = !isVisible">ToggleContent</button>

  <div>
    <h3 v-if="isLogged">Welcome {{ username }}</h3>
    <p v-else>Please Login</p>

    <p v-show="showdetails">
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Accusantium aspernatur corrupti
      similique a labore inventore neque dignissimos, minus molestiae quaerat dolorum. Quos sequi
      atque suscipit. Commodi beatae sit delectus sed.
    </p>

    <button @click="isLogged = !isLogged">ToggleLog</button>
  </div>
</template>
