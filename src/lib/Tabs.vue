<template>
  <div></div>
</template>

<script lang="ts">
import Tab from "./Tab.vue";
export default {
  setup(props, context) {
    const defaults = context.slots.default();
    defaults.forEach((tag) => {
      if (tag.type !== Tab) {
        throw new Error("Tabs 的子标签必须为Tab");
      }
    });
    return { defaults };
  },
};
</script>
