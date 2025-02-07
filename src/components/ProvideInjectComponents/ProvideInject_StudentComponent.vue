<script setup>
import { inject } from 'vue'

const studentNmae = inject('studentNmae')
const studnetage = inject('studnetage')
const studentLocation = inject('studentLocation')
</script>

<template>
  <h5>StudentNmae: {{ studentNmae }}</h5>
  <h5>Studnetage: {{ studnetage }}</h5>
  <h5>StudentLocation: {{ studentLocation }}</h5>
</template>
