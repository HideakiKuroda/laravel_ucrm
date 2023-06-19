<script setup>
import Hello from  '@/Components/Test/Hello2.vue';
import { ref } from 'vue';

const name = ref('John');
const changeName = () => {
    name.value = 'Jane';
  };
</script>

<template>
 <div id="app" class="font-sans text-center text-gray-800 mt-16">
   <h1 class="text-4xl font-bold mb-8">Vue 3 入門</h1>
   <Hello :name="name" />
   <!-- reactive な変数を props で利用したい場合には v-bind を利用する必要がある -->
   <button @click="changeName" class="px-4 py-1 text-white bg-blue-500 hover:bg-blue-600 rounded-md mx-2 my-1">Change Name</button>
</div>
</template>