<template>
  <div class="gulu-card" :class="{ hoverable }">
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    hoverable: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="scss">
.gulu-card {
  border: 1px solid rgb(165, 165, 165);
  padding: 10px 6px;
  border-radius: 5px;
  transition: all 0.5s ease-in;
}

.hoverable:hover {
  box-shadow: 2px 2px 5px 2px rgba(172, 172, 172,0.5);
  transition: all 0.5s ease-in;

}
</style>
