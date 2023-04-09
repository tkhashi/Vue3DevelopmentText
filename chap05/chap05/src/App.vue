<script setup lang="ts">
import {ref} from "vue";

const inputNameBind = ref("しんちゃ");
const inputNameOn = ref("ななし");
const onInputName = (event: Event): void => {
  const element = event.target as HTMLInputElement;
  inputNameBind.value = element.value;
}
</script>

<template>
  <section>
    <input type="text" v-model="inputNameBind">
    <p>{{ inputNameBind }}</p>
  </section>
  <br>
  <!-- <section>
    <input type="text" v-on:input = "onInputName">
    <p>{{ inputNameOn }}</p>
  </section> -->
</template>
