<template>
  <div>Button</div>
  <Button>我是按钮</Button>
  <Button theme="button">我是按钮</Button>
  <Button theme="link">我是按钮</Button>
  <Button theme="text">我是按钮</Button>
</template>

<script lang="ts">
import Button from "../lib/Button.vue";
export default {
  components: {
    Button,
  },
  setup() {
    const onClick = () => {
      console.log("hi");
    };
    return {
      onClick,
    };
  },
};
</script>
