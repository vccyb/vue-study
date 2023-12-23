<template>
  <TreeComponent :data="treeData" />
</template>

<script setup lang="ts">
import TreeComponent from "./TreeComponent.vue";
import { ref } from "vue";
const treeData = ref([
  {
    key: "1",
    title: "parent 1",
    children: [
      {
        key: "1-1",
        title: "child1",
      },
      {
        key: "1-2",
        title: "child2",
        children: [
          {
            key: "1-2-1",
            title: "grandchild1",
          },
          {
            key: "1-2-2",
            title: "grandchild2",
          },
        ],
      },
    ],
  },
  {
    key: "2",
    title: "parent 2",
    children: [
      {
        key: "2-1",
        title: "child 1",
        children: [
          {
            key: "2-1-1",
            title: "grandchild1",
          },
          {
            key: "2-1-2",
            title: "grandchild2",
          },
        ],
      },
      {
        key: "2-2",
        title: "child 2",
      },
    ],
  },
  {
    key: "3",
    title: "parent 3",
  },
]);
</script>

<style scoped></style>
