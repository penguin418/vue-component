<template>
  <div>
    <h1>두번째 양식</h1>
    <FormTwoSummary :value="value" v-on="$listeners" />
    <FormTwoDetail :value="value" v-on="$listeners" />
  </div>
</template>

<script>
import FormTwoDetail from "./FormTwoDetail.vue";
import FormTwoSummary from "./FormTwoSummary.vue";

export default {
  components: { FormTwoSummary, FormTwoDetail },
  props: {
    value: { type: Object, default: () => ({}) },
  },
};
</script>

<style></style>
