<script setup lang="ts">
import { ref } from 'vue'
const cooktailListInit = new Map<number, string>();
cooktailListInit.set(2345, 'white lady');
cooktailListInit.set(6789, 'blue hawai');
cooktailListInit.set(1234, 'new york');
const cooktailList = ref(cooktailListInit)
</script>

<template>
  <ul>
    <li v-for="[id, cookTailName] in cooktailList"
        v-bind:key="id">
        IDが{{ id }}のカクテルは{{ cookTailName }}
    </li>
  </ul>
</template>
