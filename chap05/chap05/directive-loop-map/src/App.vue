<script setup lang="ts">
import { ref } from 'vue'
const whiteLadyInit: {
  id: number
  name: string
  price: number
  recipe: string
} = {
  id: 1234,
  name: 'white lady',
  price: 1200,
  recipe: 'ほげふが'
}
const whiteLady = ref(whiteLadyInit)
</script>

<template>
  <dt>
    <template v-for="(val, key) in whiteLady" v-bind:key="key">
      <dt>{{ key }}</dt>
      <dd>{{ val }}</dd>
    </template>
  </dt>
</template>
