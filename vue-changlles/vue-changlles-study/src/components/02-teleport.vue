<script setup>
const msg = "Hello World";
</script>

<template>
  <!-- 将以下元素渲染成`body`的子元素 -->
  <Teleport to="body">
    <span>{{ msg }}</span>
  </Teleport>
</template>
