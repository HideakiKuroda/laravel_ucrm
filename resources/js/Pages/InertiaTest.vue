<script setup>
import { Link } from '@inertiajs/inertia-vue3';
import { ref } from 'vue';

const newTitle = ref('')
const newCntent = ref('')

</script>

<template>
    Inartiaテストです。<br>
    <a href="/">aタグ経由です。</a>
    <Link href="/">Link経由です。</Link> <br>
    <Link v-bind:href="route('Inertia.Index')">名前付きルート</Link><br>
    <Link :href="route('Inertia.Show', { id: 1 })">ルートパラメーターのテストです</Link>

    <div class="mb-8"></div>
    <input type="text" name="newTitle" v-model="newTitle">{{ newTitle }}<br>
    <input type="text" name="newContent" v-model="newCntent">{{ newCntent }}  <br>
    <Link as="button" method="post" :href="route('Inertia.Store')" 
    :data="{
        title:newTitle,
        content:newCntent
        }">保存テスト</Link>

</template>