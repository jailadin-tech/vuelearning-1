<script setup>
const myname = "jailadin";
const number = "1000";
function add(a,b) {
    return a+b;
}
</script>

<template>
    <h4>Name: {{ myname }}</h4>
    <h5>Number: {{ number }}</h5>
    <p>Add two numbers : {{ add(2,3) }}</p>
</template>