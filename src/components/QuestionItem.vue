<template>
  <div class="form-group" @change="inputChange">
    <h4>{{ title }}</h4>
    <slot></slot>
  </div>
</template>


<script>
export default {
  name: "Question",
  props: {
    title: String
  },
  methods: {
    inputChange(e) {
      this.$emit("inputChange", e);
    }
  }
};
</script>