<script setup>
import { ref } from "vue";

const count = ref(0);

setInterval(() => {
  count.value++;
}, 1000);
</script>

<template>
  <span v-once>使它从不更新: {{ count }}</span>
</template>
