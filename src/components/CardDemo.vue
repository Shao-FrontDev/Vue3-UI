<template>
  <Excode subheading="Card">
    <Card hoverable>Hello world</Card>
  </Excode>
</template>

<script lang="ts">
import Excode from "./Excode.vue";
import Card from "../lib/Card.vue";
export default {
  components: {
    Card,
    Excode,
  },
};
</script>
