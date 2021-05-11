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
  </div>
</template>

<script lang="ts">
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

    const f2 = () => {};
    return {
      x,
      toggle,
      f1,
      f2,
    };
  },
};
</script>
