<script setup>
import { inject } from 'vue'

const studentname = inject('studentNmae')
const schedules = inject('examsSchedule')
</script>

<template>
  <h4>Exams Schedules:{{ studentname }}</h4>

  <ul>
    <li v-for="({ name, date }, index) in schedules" :key="index">{{ name }} - {{ date }}</li>
  </ul>
</template>
