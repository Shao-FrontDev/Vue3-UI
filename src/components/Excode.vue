<template>
  <div>
    <div class="code-name">{{ subheading }}</div>
    <div class="ex-code-box">
      <slot></slot>
    </div>
    <div class="details">Code Preview</div>
    <div class="showcode">
      <slot name="code"></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    subheading: {
      type: String,
      default: "Example",
    },
  },
};
</script>

<style lang="scss">
.code-name {
  text-transform: uppercase;
  font-weight: bold;
  font-size: 16px;
}
.ex-code-box {
  margin-top: 20px;
  border: 2px solid rgb(197, 197, 197);
  border-radius: 5px;
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
  padding: 20px;
}
.details {
  margin-bottom: 100px;
  padding: 10px;
  padding-left: 20px;
  background: #e2e1e1;
  border: 2px solid rgb(197, 197, 197);
  border-radius: 5px;
  border-top-left-radius: 0;
  border-top-right-radius: 0;
  border-top: none;
  cursor: pointer;
}
</style>
