<script setup lang="ts">
import { ref } from 'vue'

const cocktailDataListInit: Cocktail[] =[
  {id: 2345, name: "white", price:1200},
  {id: 2346, name: "black", price:1201},
  {id: 2347, name: "red", price:1202}
]

const cocktailDataList= ref(cocktailDataListInit);

interface Cocktail{
  id: number;
  name: string;
  price: number;
}

</script>

<template>
  <ul>
    <li v-for="item in cocktailDataList" v-bind:key="item.id">
      {{ item.name }}の値段は{{ item.price }}円円
    </li>
  </ul>
</template>
