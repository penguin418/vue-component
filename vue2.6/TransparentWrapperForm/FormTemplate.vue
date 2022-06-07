<template>
  <component :is="component" :value="value" @update="update" />
</template>

<script>
import FormTwo from "./FormTwo";
import FormOne from "./FormOne";
export default {
  components: { FormTwo, FormOne },
  props: {
    value: { type: Object, default: () => ({}) },
  },
  computed: {
    component() {
      if (this.value.tp === "facebook") return "FormOne";
      else return "FormTwo";
    },
  },
  methods: {
    update(value) {
      this.$emit("input", value);
    },
  },
};
</script>

<style></style>
