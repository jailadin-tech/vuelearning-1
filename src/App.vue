<script setup>
import MyComponent from './components/MyComponent.vue'
import ModuleStyling from './components/ModuleStyling.vue'
import EventComponent from './components/EventsComponent.vue'
import ReactiveComponent from './components/ReactiveComponent.vue'
import RefComponent from './components/RefComponent.vue'
import ComputedPropertyComponent from './components/ComputedPropertyComponent.vue'
import ConditionalRenderingComponent from './components/ConditionalRenderingComponent.vue'
import VForComponents from './components/VForComponents.vue'
import PropsMainComponent from './components/PropsMainComponent.vue'
import ComponentEventParentComponent from './components/ComponentEventParentComponent.vue'
import ChildComponentEvent from './components/ComponentEvent/ChildComponentEvent.vue'
import { ref } from 'vue'
const registeUser = (username, email, phone) => {
  console.log(username)
  console.log(email)
  console.log(phone)
}
</script>

<template>
  <!-- <MyComponent/> -->
  <!-- <ModuleStyling /> -->
  <!--  <EventComponent /> -->
  <!-- <ReactiveComponent /> -->
  <!-- <RefComponent /> -->
  <!--   <ComputedPropertyComponent /> -->

  <!--  <ConditionalRenderingComponent />
  <VForComponents /> -->

  <!-- <PropsMainComponent pageTitle="Main Component for All types of Props Practise" /> -->

  <ChildComponentEvent @userRegister="registeUser" />
</template>

<style scoped></style>
