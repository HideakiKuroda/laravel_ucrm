<script setup>
  import Hello from '@/Components/Test/Hello2.vue';
  const handleEvent = () => {
    console.log('子コンポーネントからの通知');
  };
</script>

<template>
  <h1>Vue 3 入門</h1>
  <Hello v-on:notification="handleEvent" />
</template>