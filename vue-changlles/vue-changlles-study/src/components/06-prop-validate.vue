<script setup lang="ts">
defineProps({
  type: {
    type: String,
    validate(value: string) {
      return ["primary", "ghost", "dashed", "link", "default"].includes(value);
    },
    default: "default",
  },
});
</script>

<template>
  <button>Button</button>
</template>
