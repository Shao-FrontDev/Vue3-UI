<template>
  <Excode subheading="Tabs">
    <Tabs>
      <Tab title="导航1">内容1</Tab>
      <Tab title="导航2">内容2</Tab>
    </Tabs>
  </Excode>
</template>

<script lang="ts">
import Excode from "./Excode.vue";
import Tabs from "../lib/Tabs.vue";
import Tab from "../lib/Tab.vue";
export default {
  components: {
    Tabs,
    Tab,
    Excode,
  },
};
</script>
