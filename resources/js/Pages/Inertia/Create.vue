<script setup>
import { reactive } from 'vue'
import { Inertia } from '@inertiajs/inertia'
import BreezeValidationErrors from '@/Components/ValidationErrors.vue'

const form = reactive({
    title: null,
    content: null
}) 

const submitFunction = () => {
    Inertia.post('/inertia', form)
}

defineProps({
    errors: Object
})

</script>

<template>
    <BreezeValidationErrors :errors="errors"/>
    <form @submit.prevent="submitFunction">
        <input class="px-4 py-1 rounded-md mx-2 my-1" type="text" name="title" v-model="form.title" ><br>
        <div v-if="errors.title">{{ errors.title }}</div><br>
        <input class="px-4 py-1 rounded-md mx-2 my-1" type="text" name="content" v-model="form.content"><br>
        <div v-if="errors.content">{{ errors.content }}</div><br>
        <button class="px-4 py-1 text-white bg-blue-500 hover:bg-blue-600 rounded-md mx-2 my-1">送信</button>
    </form>
</template>