<script setup>
const route = useRoute()
</script>

<template>
  <div>
    <div v-if="route.name !== 'index'">
      <a class="mx-5 block font-medium text-blue-600 dark:text-blue-500 hover:underline" href="/">
        Go back to homepage
      </a>
    </div>
    <slot />
  </div>
</template>