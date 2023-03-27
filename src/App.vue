<script setup>

  import { ref } from "vue";

const text = ref("");
const cards = ref(["1", "2", "6","24","125","720","5040","40320","362880","3628800"]);
</script>


<template>
  <input type="text" v-model=text>
  <div v-for="fctr in cards" :key=fctr>
      <h1 v-if="fctr.includes(text)">{{ fctr }}</h1>
  </div>
</template>