<template>
  <b-button :variant="variant" @click="onClick()">{{ txt }}</b-button>
</template>
<script>
export default {
  name: "LargeBtn",
  props: {
    txt: String,
    variant: String,
  },
  methods: {
    onClick() {
      this.$emit("click");
    },
  },
};
</script>
<style scoped>
button {
  border-radius: 40px;
}
</style>
