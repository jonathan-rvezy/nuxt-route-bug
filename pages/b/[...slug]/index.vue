<template>
  <NuxtLayout name="base">
    <div>
      <NuxtLink :href="`/a/${Math.random()}?q=${Math.random()}`"
      >A Page</NuxtLink
      >
    </div>
    <div>B Page</div>
  </NuxtLayout>
</template>

<script setup lang="ts">
definePageMeta({
  layout: "b",
});

const route = useRoute();

console.log({ source: "page", query: route.query, fullPath: route.fullPath });
</script>
