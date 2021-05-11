<template>
  <Excode subheading="button">
    <Button theme="button">button</Button>
    <Button theme="link">button</Button>
    <Button theme="text">button</Button>
  </Excode>

  <Excode>
    <Button size="big">大大大</Button>
    <Button>普普通</Button>
    <Button size="small">小小小</Button>
  </Excode>

  <Excode>
    <Button disabled>禁用按钮</Button>
    <Button theme="link" disabled>禁用链接按钮</Button>
    <Button theme="text" disabled>禁用按钮</Button>
  </Excode>

  <Excode>
    <Button loading>加载中</Button>
    <Button>加载完毕</Button>
  </Excode>
</template>

<script lang="ts">
import Excode from "./Excode.vue";
import Button from "../lib/Button.vue";
export default {
  components: {
    Button,
    Excode,
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
