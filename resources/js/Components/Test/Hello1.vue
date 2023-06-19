
<script setup>
import { ref, reactive } from 'vue';

  const count = ref(0);

  const state = reactive({
  count: 1,
  });

  const addRefCount = () => {
    count.value++;
  };

  const addReactiveCount = () => {
    state.count++;
  };

  const props = defineProps({
    message: {
    type: String,
    required: true,
    },
    name: { type: String, default: 'Jane' },
    price: Number,

    isAdmin: Boolean,
  });

</script>

<template>
    <h2 class="my-1">初めてのコンポーネント</h2>
    <p  class="text-2xl mb-8" >{{ props.name }} {{ props.message }}</p>
    <p>{{ props.price + 100 }}</p>

    <p class="text-1xl mb-8" v-if="props.isAdmin">管理者です。</p>
    <p class="text-1xl mb-8" v-else>管理者ではありません。</p>
    
    <!-- <p>Ref Count:{{ count }}</p>
    <p>Reactive Count:{{ state.count }}</p> -->
    <div>
    <!-- <button @click="addRefCount" class="px-4 py-1 text-white bg-blue-500 hover:bg-blue-600 rounded-md mx-2 my-1">
      Ref Count+
    </button>
    <button @click="addReactiveCount" class="px-4 py-1 text-white bg-blue-500 hover:bg-blue-600 rounded-md mx-2 my-1">
      Reactive Count+
    </button> -->

      <!-- 
      px-4 水平方向のパディング
      py-2 垂直方向のパディング
      text-white テキストカラーを白色に設定
      bg-blue-500 、背景色を青色（500レベルの色）に設定
      hover:bg-blue-600 ホバー時の背景色をより濃い青色（600レベルの色）に設定
      rounded-md ボタンの角を丸めるためのクラス
      mx-2 ボタン間に水平方向に2の幅のスペースが追加されます。
      my-1 クラスを使用して垂直方向の間隔を調整、上下に1のスペース
       -->

    </div>    
</template>