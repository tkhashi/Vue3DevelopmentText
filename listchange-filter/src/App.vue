<script setup lang="ts">
  import { ref, computed } from 'vue'
const cocktailDataListInit: Cocktail[] =[
  {id: 2345, name: "white", price:1200},
  {id: 2346, name: "black", price:1500},
  {id: 2347, name: "black", price:1201},
  {id: 2348, name: "red", price:1500}
]

const cocktailDataList= ref(cocktailDataListInit);

const cocktail1500 = computed(
  (): Cocktail[] => {
    const newList = cocktailDataList.value.filter(
      (cocktailItem: Cocktail): boolean => { 
        return cocktailItem.price == 1500;
      }
    )
    return newList
  }
);



interface Cocktail{
  id: number;
  name: string;
  price: number;
}

</script>

<template>
  <section>
    カクテルリスト
    <ul>
      <li v-for="item in cocktailDataList" v-bind:key="item.id">
        {{ item.name }}の値段は{{ item.price }}円円
      </li>
    </ul>
  </section>
  <section>
    値段が1500円のカクテル
    <ul>
      <li v-for="cocktail in cocktail1500" v-bind:key="cocktail.id">
        {{ cocktail.name }} の値段は {{ cocktail.price }}
      </li>
    </ul>
  </section>
</template>
