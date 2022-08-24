<template>
  <button @click="click" class="btn" :class="[color]">
    <slot />
  </button>
</template>
<script>
export default {
  name: "Button-Component",
  methods: {
    click() {
      this.$emit("click");
    },
  },
  props: {
    color: {
      type: String,
    },
  },
};
</script>
<style lang="scss" scoped>
@import "../assets/scss/color.scss";
.btn {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  padding: 20px;
  border-radius: 10px;
  border:none;
  cursor: pointer;
  &.button1 {
    background-color: $button1;
  }
  &.button2 {
    background-color: $button2;
  }
  &.button3 {
    background-color: $button3;
  }
}
</style>
