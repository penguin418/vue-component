<template>
  <div>
    <h1>첫번째 양식</h1>
    <FormOneSummary :value="value" v-on="$listeners" />
    <FormOneDetail :value="value" v-on="$listeners" />
  </div>
</template>

<script>
import FormOneDetail from "./FormOneDetail.vue";
import FormOneSummary from "./FormOneSummary.vue";

export default {
  components: { FormOneSummary, FormOneDetail },
  props: {
    value: { type: Object, default: () => ({}) },
  },
};
</script>

<style></style>
