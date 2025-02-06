<script setup>
import { ref } from 'vue'
const fruits = ref(['Apple', 'Banana', 'Orange', 'Grapes', 'Pineapple'])
const items = ref([
  { id: 1, name: 'Apple', price: 50 },
  { id: 2, name: 'Banana', price: 20 },
  { id: 3, name: 'Orange', price: 30 },
  { id: 4, name: 'Grapes', price: 40 },
  { id: 5, name: 'Pineapple', price: 60 },
])

const products = ref([
  {
    id: 1,
    name: 'Laptop',
    price: 1500,
    category: 'Electronics',
    details: {
      brand: 'Dell',
      model: 'XPS 13',
      specs: ['13-inch display', '16GB RAM', '512GB SSD'],
    },
  },
  {
    id: 2,
    name: 'Smartphone',
    price: 800,
    category: 'Electronics',
    details: {
      brand: 'Samsung',
      model: 'Galaxy S21',
      specs: ['6.2-inch display', '8GB RAM', '128GB storage'],
    },
  },
  {
    id: 3,
    name: 'Coffee Maker',
    price: 120,
    category: 'Home Appliances',
    details: {
      brand: 'Keurig',
      model: 'K-Classic',
      specs: ['Single-serve', 'Removable drip tray', 'Auto shut-off'],
    },
  },
  {
    id: 4,
    name: 'Headphones',
    price: 250,
    category: 'Accessories',
    details: {
      brand: 'Sony',
      model: 'WH-1000XM4',
      specs: ['Noise-canceling', 'Wireless', '30 hours battery life'],
    },
  },
  {
    id: 5,
    name: 'Electric Kettle',
    price: 60,
    category: 'Home Appliances',
    details: {
      brand: 'Hamilton Beach',
      model: 'Electric Kettle',
      specs: ['1.7L capacity', 'Stainless steel', 'Auto shut-off'],
    },
  },
])
</script>
<template>
  <ul>
    <li v-for="(item, index) in fruits" :key="index">{{ item }}</li>
  </ul>
  <hr />
  <ul>
    <li v-for="(item, i) in items" :key="i">{{ item.name }} - {{ item.price }} Rs/-</li>
  </ul>
  <hr />
  <table border="1">
    <tr>
      <td>Id</td>
      <td>Name</td>
      <td>Price</td>
      <td>Category</td>
      <td>Details</td>
    </tr>
    <tr v-for="({ id, name, price, category, details }, index) in products" :key="index">
      <td>{{ id }}</td>
      <td>{{ name }}</td>
      <td>{{ price }}</td>
      <td>{{ category }}</td>
      <td>
        <span v-for="(value, key, i) in details" :key="i">{{ value }}<br /></span>
      </td>
    </tr>
  </table>
</template>
