<script setup>
  defineProps(['title','itemList'])
</script>

<template>
  <div class="m-2">
    <div class="text-lg font-bold" v-if="title">
    {{ title }}
  </div>
  <ul class="list-disc" v-for="item in itemList" :key="item">
    <li>
      {{ item }}
    </li>
  </ul>
  </div>
</template>