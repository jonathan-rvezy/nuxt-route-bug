<template>
  <NuxtLayout name="base">
    <div>A Page</div>
    <div>
      <NuxtLink :href="`/b/${Math.random()}?q=${Math.random()}`"
        >B Page</NuxtLink
      >
    </div>
  </NuxtLayout>
</template>

<script setup lang="ts">
definePageMeta({
  layout: "a",
});

const route = useRoute();

console.log({ source: "page", query: route.query, fullPath: route.fullPath });
</script>
