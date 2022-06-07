<template>
  <div>
    첫번째 양식 상세
    <korean-input v-model="form.name" />
  </div>
</template>

<script>
import KoreanInput from "../KoreanInput.vue";
export default {
  components: { KoreanInput },
  props: {
    value: { type: Object, default: () => ({}) },
  },
  data() {
    return {
      form: { ...{ tp: "", name: "" }, ...this.value },
    };
  },
  watch: {
    value: {
      deep: true,
      handler() {
        this.form = this.value;
      },
    },
    form: {
      deep: true,
      handler() {
        this.$emit("update", this.form);
      },
    },
  },
};
</script>

<style></style>
