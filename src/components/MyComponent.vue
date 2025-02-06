<script setup>
const myname = "jailadin";
const number = "1000";
function add(a,b) {
    return a+b;
}
const myRefLink ="https://youtu.be/pgWZLS75Nmo?si=_ESvwoNg9-1QqPvc";
const myImage = "https://ik.imagekit.io/laracasts/series/thumbnails/svg/learn-vue-3.svg?tr=w-200";
const altText ="Random Image";
</script>

<template>
    <h4>Name: {{ myname }}</h4>
    <h5>Number: {{ number }}</h5>
    <p>Add two numbers : {{ add(2,3) }}</p>
    <p>
        <a :href="myRefLink">Ref. Video Link</a>
    </p>
    <p> 
        <img :src="myImage" alt="{{ altText }}">
    </p>
</template>