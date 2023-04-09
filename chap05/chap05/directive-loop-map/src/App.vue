<script setup lang="ts">
import { ref } from 'vue'
const cooktailListInit: {[key: number]: string} ={
  2345: 'white lady',
  6789: 'blue hawai',
  1234: 'new york'
} 
const cooktailList = ref(cooktailListInit)
</script>

<template>
  <ul>
    <li v-for="(cookTailName, id) in cooktailList"
        v-bind:key="'cookTailName' + id">
        IDが{{ id }}のカクテルは{{ cookTailName }}
    </li>
  </ul>
  <ul>
    <li v-for="(cookTailName, id, index) in cooktailList"
        v-bind:key="'cookTailListwithIdx' + id">
        {{ index + 1 }}: IDが{{ id }}のカクテルは{{ cookTailName }}
    </li>
  </ul>
</template>
