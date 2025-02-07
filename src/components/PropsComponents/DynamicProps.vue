<script setup>
const nameProp = defineProps(['firstname', 'surname'])
</script>
<template>
  <h4>Full Name : {{ nameProp.firstname }} {{ nameProp.surname }}</h4>
</template>
