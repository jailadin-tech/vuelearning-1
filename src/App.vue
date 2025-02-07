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
import ChildComponentEvent from './components/ComponentEvent/ChildComponentEvent.vue'

import { ref } from 'vue'
import SlotComponent from './components/SlotComponents/SlotComponent.vue'
import FallbackContent from './components/SlotComponents/FallbackContent.vue'
import MyNamedSlot from './components/SlotComponents/My-NamedSlot.vue'
import MyDefaultSlot from './components/SlotComponents/My-DefaultSlot.vue'

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

  <!-- <ChildComponentEvent @userRegister="registeUser" /> -->

  <!-- Pass content into slotcomponent -->
  <SlotComponent>
    <h4>Content 1 will go to slot area</h4>
    <h4>Content 2 will go to slot area</h4>
  </SlotComponent>
  <!-- When no data/content passed then defult/fallback content will be show -->
  <FallbackContent> </FallbackContent>

  <MyNamedSlot>
    <template v-slot:one> <h4>Content will go into slot one</h4></template>
    <template #two> <h4>Content will go into slot two</h4></template>
  </MyNamedSlot>
  <MyDefaultSlot #default> </MyDefaultSlot>
</template>

<style scoped></style>
