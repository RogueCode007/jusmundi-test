<script setup>
import Icon from "./Icon.vue";

defineProps({
  iconSrc: String,
  header: String,
  content: String,
});
</script>
<template>
  <div>
    <Icon :src="iconSrc" />
    <h4>{{ header }}</h4>
    <p>{{ content }}</p>
  </div>
</template>

<style lang="scss" scoped>
div {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  gap: 10px;
  padding: 32px 5px;
}
:deep(img) {
  width: 48px;
  height: 48px;
  display: block;
}
h4 {
  font-weight: bold;
  font-size: 18px;
  line-height: 32px;
  text-align: center;
}
p {
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
  text-align: center;
}
</style>
