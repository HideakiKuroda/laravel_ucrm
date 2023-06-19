<script setup>
import { Inertia } from '@inertiajs/inertia';

defineProps({
    id : String,
    blog : Array
})

const deleteConfirm = (id) => {
    // console.log(id)
    Inertia.delete(`/inertia/${id}` , { //バッククォートを使う
        onBefore: () => confirm('本当に削除しますか？')
    })
}
</script>

<template>
    {{ id }}<br>
    {{ blog.title }}
    <button @click="deleteConfirm(blog.id)">削除</button>
</template>

