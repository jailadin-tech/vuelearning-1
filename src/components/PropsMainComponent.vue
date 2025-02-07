<script setup>
const pageName = defineProps(['pageTitle'])

import { ref } from 'vue'

import DynamicProps from './PropsComponents/DynamicProps.vue'
import StaticProp from './PropsComponents/StaticProp.vue'
import PropsDataValidator from './PropsComponents/PropsDataValidator.vue'
import PropsTypeValidation from './PropsComponents/PropsTypeValidation.vue'

const firstname = ref('Jailadin')
const lastname = ref('Shaik')

const amount = ref(100)
const specifications = ref(['12GB RAM', 'MediaTech Processor'])
const invoicenumer = 'SDF87821165'
const customerInfo = ref({ name: 'Raju', Mobile: '8897', city: 'Guntur' })

const employeeInfo = ref({ name: 'Raju', Mobile: ['8897', '9059'], age: 30 })
const empProfessionInfo = ref({
  company: '5Y',
  expected_ctc: 1300000,
  jobtype: ['Remote', 'Hybric'],
})
const techSkills = ref(['PHP', 'MYSQL', 'LARAVEL', 'VUE', 'HTML'])
</script>

<template>
  <h2>{{ pageName.pageTitle }}</h2>
  <hr />
  <StaticProp wishing="Hello" />

  <DynamicProps :firstname="firstname" :surname="lastname" />
  <PropsTypeValidation
    :invoice="invoicenumer"
    :amount="amount"
    product="IQU 7PRO"
    :specs="specifications"
    :customerInfo="customerInfo"
  />
  <PropsDataValidator
    :personal="employeeInfo"
    :professional="empProfessionInfo"
    :skills="techSkills"
    expectedLocations="Hyderabad"
  />
</template>
