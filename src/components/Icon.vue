<script setup lang="ts">
defineProps({
  src: String,
});
</script>
<template>
  <img :src="`src/assets/svg/${src}.svg`" />
</template>

<style scoped></style>
