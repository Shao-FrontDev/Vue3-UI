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
  <br />
  <hr />
  <br />
  <h1>示例3</h1>
  <br />
  <div>
    <Button disabled>禁用按钮</Button>
    <Button theme="link" disabled>禁用链接按钮</Button>
    <Button theme="text" disabled>禁用按钮</Button>
  </div>
  <br />
  <hr />
  <br />
  <h1>示例4</h1>
  <br />
  <div>
    <Button loading>加载中</Button>
    <Button>加载完毕</Button>
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
