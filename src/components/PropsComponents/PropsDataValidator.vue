<script setup>
const Props = defineProps({
    personal: {
    type: Object,
    validator: (item) => {
      // Validate each field in 'personal' object
      return (
        typeof item.name === 'string' &&
        Array.isArray(item.Mobile) &&
        item.Mobile.every(mob => /^\d+$/.test(mob)) && // Validate mobile numbers
        typeof item.age === 'number' && item.age >= 25 && item.age <= 31
      )
    },
  },
  professional: {
    type: Object,
    validator: (item) => {
       // Validate each field in 'professional' object
       return (
        typeof item.company === 'string' &&
        typeof item.expected_ctc === 'number' &&
        item.expected_ctc <= 1500000 && // Validate expected_ctc
        Array.isArray(item.jobtype) && item.jobtype.every(job => typeof job === 'string') // Validate each location
      )
    },
  },
  expectedLocations:{
      type:String,
    validator:(loc)=>  ['Hyderabad','VZD','Chennai'].includes(loc)
  },
  skills: {
    type: Array,
    validator: (item) => {
      return    item.every( (skill) => typeof skill === 'string' ) 
    },
  },
}) 
</script>
<template>
  <h4>Candidate Info</h4>

  <p>Personal:
  <ul v-for="(value, key, index) in personal" :key="index">
    <li>{{ key }}:{{ value }}</li>
  </ul>
</p>
<p>Professional:
  <ul v-for="(value, key, index) in professional" :key="index">
    <li>{{ key }}:{{ value }}</li>
  </ul>
</p>
  <p>
    Skills : <span v-for="(skill, index) in skills" :key="index">-- {{ skill }}</span>
  </p>
</template>
