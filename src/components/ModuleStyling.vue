<template>
  <!--   <h1 class="local-style">Local Styling the element</h1>-->
  <!-- <h2 :class="$style['mystyle']">Module styling</h2> -->
  <h2 :class="myclasses.mystyle">Module styling</h2>
</template>

<!-- Module styling -->
<style module="myclasses">
.mystyle {
  background-color: seagreen;
  color: wheat;
}
</style>

<!-- Localstyle  -->
<!-- <style scoped>
.local-style {
  background-color: firebrick;
  color: wheat;
}
</style> -->
