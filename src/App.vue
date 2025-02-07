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

import { provide, ref } from 'vue'
import SlotComponent from './components/SlotComponents/SlotComponent.vue'
import FallbackContent from './components/SlotComponents/FallbackContent.vue'
import MyNamedSlot from './components/SlotComponents/My-NamedSlot.vue'
import MyDefaultSlot from './components/SlotComponents/My-DefaultSlot.vue'
import ProvideInject_SchoolComponent from './components/ProvideInjectComponents/ProvideInject_SchoolComponent.vue'

const registeUser = (username, email, phone) => {
  console.log(username)
  console.log(email)
  console.log(phone)
}
/* Provide: specified data in provide , will go to child or nexted child who need this and they inject this to their component */
provide('studentNmae', 'jailadin')
provide('studnetage', 30)
provide('studentLocation', ['Guntur', 'Hyderbad'])

const fruits = ref(['Apple', 'Banana', 'Orange', 'Grapes', 'Pineapple'])
const examsList = ref([
  { id: 1, name: 'UnitTest 1', date: '10-01-2025' },
  { id: 2, name: 'UnitTest 2', date: '15-01-2025' },
  { id: 3, name: 'SemTest 1', date: '10-02-2025' },
  { id: 4, name: 'SemTest 2', date: '10-03-2025' },
  { id: 5, name: 'FinalTest', date: '20-03-2025' },
])
provide('examsSchedule', examsList)
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
  <!-- <SlotComponent>
    <h4>Content 1 will go to slot area</h4>
    <h4>Content 2 will go to slot area</h4>
  </SlotComponent>
  <FallbackContent> </FallbackContent>
  <MyNamedSlot>
    <template v-slot:one> <h4>Content will go into slot one</h4></template>
    <template #two> <h4>Content will go into slot two</h4></template>
  </MyNamedSlot>
  <MyDefaultSlot #default> </MyDefaultSlot> -->

  <ProvideInject_SchoolComponent />
</template>

<style scoped></style>
