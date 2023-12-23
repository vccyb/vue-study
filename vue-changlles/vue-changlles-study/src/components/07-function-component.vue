<script setup lang="ts">
import { ref, h } from "vue";

interface ListProps {
  "adtive-index": number;
  list: Array<{ name: string }>;
  onToggle: (index: number) => void;
}

/**
 * 实现该函数式组件 :
 * 1. 使用`list`数据渲染列表元素 (ul/li)
 * 2. 当点击列表子元素时,将其文本颜色更改为红色
 */
const ListComponent = (props: ListProps) => {
  return h(
    "ul",
    null,
    props.list.map((item, index) =>
      h(
        "li",
        {
          key: index,
          style: { color: props["active-index"] === index ? "red" : null },
          onClick: props.onToggle.bind(null, index),
        },
        item.name
      )
    )
  );
};

const list = [
  {
    name: "John",
  },
  {
    name: "Doe",
  },
  {
    name: "Smith",
  },
];

const activeIndex = ref(0);

function toggle(index: number) {
  activeIndex.value = index;
}
</script>

<template>
  <list-component :list="list" :active-index="activeIndex" @toggle="toggle" />
</template>
