<script setup>
/* Counting */
import { ref } from 'vue'
const count = ref(0)
/* show Message */
const showmessage = (message) => {
  alert(message + '' + count.value)
}
/* Form handling */
const formHandler = (e) => {
  e.preventDefault()
  alert('form submited')
}
</script>
<template>
  <h4>Count: {{ count }}</h4>
  <button v-on:click="count++">Increment</button>
  <button v-on:click="count--">Decrement</button>
  <br />
  <br />
  <button @:click="showmessage('Current Counting is: ')">ShowMessage</button>
  <br />
  <br />
  <form action="" v-on:submit="formHandler">
    <input type="text" name="UserName" id="" />
    <input type="text" name="PhoneNo" id="" />
    <button type="submit">Submit</button>
  </form>
</template>
