<script setup lang="ts">
defineProps<{
  title: string;
  subtitle: string;
}>();
</script>

<template>
  <div>
    <h1 class="w-full p-12 text-6xl text-center">{{ title }}</h1>
    <h3>{{ subtitle }}</h3>
  </div>
</template>
