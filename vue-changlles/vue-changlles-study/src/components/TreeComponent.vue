<script setup lang="ts">
interface TreeData {
  key: string;
  title: string;
  children: TreeData[];
}
defineProps<{ data: TreeData[] }>();
</script>

<template>
  <div v-for="item in data" :key="key">
    <div style="margin-left: 100px">
      <div>{{ item.title }}</div>
      <TreeComponent v-if="item?.children?.length" :data="item.children" />
    </div>
  </div>
</template>
