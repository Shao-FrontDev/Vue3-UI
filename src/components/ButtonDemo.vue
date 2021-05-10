<template>
  <h3>示例1</h3>
  <br />
  <div>
    <Button theme="button">button</Button>
    <Button theme="link">button</Button>
    <Button theme="text">button</Button>
  </div>
  <br />
  <hr />
  <br />
  <h3>示例2</h3>
  <br />
  <div>
    <Button size="big">大大大</Button>
    <Button>普普通</Button>
    <Button size="small">小小小</Button>
  </div>
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
