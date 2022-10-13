<script setup lang="ts">
import TheTitle from "./components/TheTitle.vue";
import TheList from "./components/TheList.vue";
</script>

<template>
  <header>
    <div class="w-full text-center bg-white">
      <TheTitle
        title="☕Everything I brew, I brew for you."
        subtitle="Who is going to be brewing your tea today?"
      />
    </div>
  </header>

  <main><TheList /></main>
</template>
