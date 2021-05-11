<template>
  <div>
    <header>标题</header>
    <main>
      <p>hello world</p>
      <p>hello world</p>
    </main>
    <footer>
      <Button>OK</Button>
      <Button>Cancel</Button>
    </footer>
  </div>
</template>

<script lang="ts">
import Button from "./Button.vue";
export default {
  components: {
    Button,
  },
};
</script>
