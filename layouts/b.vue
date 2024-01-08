<template>
  <div>Layout B</div>
  <slot />
</template>

<script lang="ts" setup>
const route = useRoute();

console.log({ source: "layout", query: route.query, fullPath: route.fullPath });
</script>
