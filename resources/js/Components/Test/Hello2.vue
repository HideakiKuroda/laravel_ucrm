<script setup>
const props = defineProps({
  name: String,
});
</script>

<template>
  <!-- <h2 class="text-1xl mb-8">子コンポーネント</h2>
  <p class="text-1xl mb-8">Hello {{ props.name }}</p> -->
  <div>
    <h2>子コンポーネント</h2>
    <button @click="$emit('notification')">通知</button>
  </div>
</template>