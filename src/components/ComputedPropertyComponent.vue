<script setup>
import { ref, computed } from 'vue'

/* Computed: automatically update itself, when data it depends on changes. Its like a worker that wathes certain data ,  perform some work on it , and always provide up-to-date result */

const number = ref(10)
const squerNumber = computed(() => {
  return number.value * number.value
})

const counter = ref(0)
const incrementCounter = () => {
  counter.value++
}
const squerCounter = computed(() => {
  return counter.value ** 2
})

const firstname = ref('jailadin')
const lastname = ref('shaik')
const fullname = computed(() => {
  return firstname.value + '' + lastname.value
})
</script>
<template>
  <h4>Count: {{ counter }}</h4>
  <h5>Squred Counter: {{ squerCounter }}</h5>
  <button @click="incrementCounter">Increse Counter</button>
  <hr />
  <h4>FullName : {{ fullname }}</h4>
  <hr />
  <h4>Number: {{ number }}</h4>
  <h5>Squred Number: {{ squerNumber }}</h5>
</template>
