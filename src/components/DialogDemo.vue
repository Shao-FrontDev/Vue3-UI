<template>
  <div>
    <div>Dialog</div>

    <Button @click="toggle">toggle</Button>

    <Dialog v-model:visible="x" :ok="f1" :cancel="f2">
      <template v-slot:content>
        <div>Hello world</div>
      </template>
      <template v-slot:title>
        <div>
          <h3>Github</h3>
        </div>
      </template>
    </Dialog>
    <h2>示例2</h2>
    <Button @click="showDialog">toggle</Button>
  </div>
</template>

<script lang="ts">
import { openDialog } from "../lib/openDialog.ts";
import Dialog from "../lib/Dialog.vue";
import Button from "../lib/Button.vue";
import { ref, Ref } from "vue";
export default {
  components: {
    Dialog,
    Button,
  },
  setup() {
    const x = ref(false);
    const toggle = () => {
      console.log("toggle");
      x.value = !x.value;
      console.log(x.value);
    };
    const f1 = () => {
      console.log("f1");
      return false;
    };

    const showDialog = () => {
      openDialog({
        title: "标题",
        content: "你好",
        ok() {
          console.log("ok");
        },
        cancel() {
          console.log("cancel");
        },
      });
    };

    const f2 = () => {};
    return {
      x,
      toggle,
      f1,
      f2,
      showDialog,
    };
  },
};
</script>
