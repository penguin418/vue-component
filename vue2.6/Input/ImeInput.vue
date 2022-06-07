<template>
  <input :value="value" @input="input" v-bind="$attrs" v-on="listeners" />
</template>

<script>
export default {
  name: "ImeInput",
  props: { value: { type: String, default: "" } },
  computed: {
    listeners() {
      const { input, ...listeners } = this.$listeners;
      return listeners;
    },
  },
  methods: {
    input(event) {
      this.$emit("input", event.target.value);
    },
  },
};
</script>

<style></style>
