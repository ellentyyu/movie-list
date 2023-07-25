<template>
  <main>
    {{num}}
    <input type="text" v-model="num">

    <button @click="num++">按鈕</button>
  </main>
</template>

<script setup>
import { ref } from 'vue'
const num = ref(5);
</script>