<script setup>
  import Hello from '@/Components/Test/Hello1.vue';

</script>

<template>
  <div id="app" class="font-sans text-center text-gray-800 mt-16">
    <h1 class="text-4xl font-bold mb-8">Vue 3 入門</h1>
    <!-- <Hello message="Propsの使い方"  />
    <Hello message="defineProps関数を利用" /> -->
    <Hello  v-bind:price="1000"  :isAdmin="false" />
    <!-- props で数値やBooleanを渡したい場合は v-bind の設定を行います設定を行わないと文字列が渡されます。 -->
    <!-- v-bind ディレクティブは:の省略形で記述することができます。 -->
  </div>
</template>


<!-- 
<div id="app"> 
  font-sans（サンセリフフォント）  
  text-center（中央揃え）
  text-gray-800（ダークグレーのテキストカラー）
  mt-16（上側のマージン）

<h1> 要素
  text-4xl（4倍の大きさのテキスト）
  font-bold（太字）
  mb-8（下側のマージン）
 -->


