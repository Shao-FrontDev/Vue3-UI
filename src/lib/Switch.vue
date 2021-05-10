<template>
  <button
    class="gulu-switch"
    :class="{ checked: value }"
    @click="toggle"
  >
    <span></span>
  </button>
  <div>{{ value }}</div>
</template>

<script lang="ts">
export default {
  props: {
    value: Boolean,
  },
  setup(props, context) {
    const toggle = () => {
      context.emit("update:value", !props.value);
    };
    return {
      toggle,
    };
  },
};
</script>

<style lang="scss">
$h: 22px;
$h2: $h - 4px;
.gulu-switch {
  height: $h;
  width: $h * 2;
  border: none;
  background: rgba(0, 0, 0, 0.25);
  border-radius: $h/2;
  position: relative;
  transition: all 0.5s;
  > span {
    position: absolute;
    top: 2px;
    left: 2px;
    height: $h2;
    width: $h2;
    background: white;
    border-radius: $h2 / 2;
    transition: all 1s;
  }
  &.checked {
    background: #1890ff;
  }
}

.gulu-switch.checked > span {
  left: calc(100% - #{$h2} - 2px);
}

.gulu-switch:focus {
  outline: none;
}
</style>
