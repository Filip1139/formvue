<template>
  <div class="form-check">
    <input class="form-check-input" type="radio" :name="name" :id="id" :value="value" />
    <label class="form-check-label" :for="id">{{ title }}</label>
  </div>
</template>

<script>
export default {
  name: "Radio",
  props: {
    name: String,
    id: String,
    value: String,
    title: String
  }
};
</script>

