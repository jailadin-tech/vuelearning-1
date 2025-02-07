<script setup>
const Props = defineProps({
  invoice: [String, Number],
  amount: {
    type: Number,
    required: true,
    default: 0,
  },
  product: {
    type: String,
    required: true,
    default: 'Random Text',
  },
  specs: Array,
  customerInfo: Object,
})
</script>
<template>
  <h4>Sale Details</h4>
  <p>
    Invoice Number : {{ Props.invoice }} -- Product : {{ Props.product }} -- Amount :
    {{ Props.amount }}
  </p>
  <p>
    Specifications : <span v-for="(itemspec, index) in specs" :key="index">-- {{ itemspec }}</span>
  </p>

  <p>CustomerInfo:</p>
  <ul v-for="(value, key, index) in customerInfo" :key="index">
    <li>{{ key }}:{{ value }}</li>
  </ul>
</template>
