<script setup>
// import {Head, Link } from '@inertiajs/vue3';

</script>

<template>
    <div id="app">
  <div id="gantt-header" class="h-12 p-2 flex items-center">
    <h1 class="text-xl font-bold">ガントチャート</h1>
  </div>
  <div id="gantt-content" class="flex">
    <div id="gantt-task">
      <div
        id="gantt-task-title"
        class="flex items-center bg-green-600 text-white h-20"
      >
        <div
          class="border-t border-r border-b flex items-center justify-center font-bold text-xs w-48 h-full"
        >
          タスク
        </div>
        <div
          class="border-t border-r border-b flex items-center justify-center font-bold text-xs w-24 h-full"
        >
          開始日
        </div>
        <div
          class="border-t border-r border-b flex items-center justify-center font-bold text-xs w-24 h-full"
        >
          完了期限日
        </div>
        <div
          class="border-t border-r border-b flex items-center justify-center font-bold text-xs w-16 h-full"
        >
          担当
        </div>
        <div
          class="border-t border-r border-b flex items-center justify-center font-bold text-xs w-12 h-full"
        >
          進捗
        </div>
      </div>
    </div>
    <div id="gantt-calendar">カレンダー領域</div>
  </div>
</div>
</template>