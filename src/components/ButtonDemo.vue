<template>
  <Button>button</Button>
  <Button theme="button">button</Button>
  <Button theme="link">button</Button>
  <Button theme="text">button</Button>
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
