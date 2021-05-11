<template>
  <Excode subheading="Switch">
    <Switch v-model:value="bool" />
  </Excode>
</template>

<script lang="ts">
import Excode from "./Excode.vue";
import Switch from "../lib/Switch.vue";
import { ref } from "vue";
export default {
  components: {
    Switch,
    Excode,
  },
  setup() {
    const bool = ref(true);
    return { bool };
  },
};
</script>
