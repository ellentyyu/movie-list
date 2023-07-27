<template>
    <main>
        {{num}}
        <input type="text" v-model="num">

        <button @click="num++">按鈕</button>
        <div class="container mx-auto p-4 bg-stone-100">
            <div class="flex justify-between space-x-4">
                <div class="flex-auto bg-indigo-200 p-5 rounded">233</div>
                <div class="flex-auto bg-indigo-200 p-5 rounded">343</div>
                <div class="flex-auto bg-indigo-200 p-5 rounded">好看的</div>
                <div class="flex-auto bg-indigo-200 p-5 rounded">tar</div>
            </div>
        </div>
    </main>
</template>

<script setup>
import { ref } from 'vue'
const num = ref(5);
</script>