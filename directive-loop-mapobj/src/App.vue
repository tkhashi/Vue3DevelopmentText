<script setup lang="ts">
  import { ref } from 'vue'
  const cocktailDataListInit = new Map<number, Cocktail>();
  cocktailDataListInit.set(1234, {id: 1234, name: "white lady", price: 1200});
  cocktailDataListInit.set(2346, {id: 2346, name: "black", price:1500});
  cocktailDataListInit.set(2347, {id: 2347, name: "red", price:1202});
  cocktailDataListInit.set(2348, {id: 2348, name: "blue", price:1500});

  const cocktailDataList= ref(cocktailDataListInit);

  interface Cocktail{
    id: number;
    name: string;
    price: number;
  }

</script>

<template>
  <!-- cocktailDataListの値をイテレートしてnameとpriceを表示する -->
  <ul>
    <li v-for="[id, cocktail] in cocktailDataList" :key="id">
      <p>{{cocktail.name}}</p>
      <p>{{cocktail.price}}</p>
    </li>
  </ul>
</template>
