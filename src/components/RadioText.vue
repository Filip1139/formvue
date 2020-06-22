<template>
  <div class="form-check">
    <input class="form-check-input" type="radio" :name="name" :id="id" @click="showInput" />
    <label class="form-check-label" :for="id">{{ title }}</label>
    <input type="text" :class="{'visible': isVisible}" v-model="isVisible" />
    <p>{{isVisible}}</p>
  </div>
</template>

<script>
export default {
  name: "RadioText",
  data() {
    return {
      isVisible: false
    };
  },
  props: {
    name: String,
    id: String,
    value: String,
    title: String,
    isChecked: Object
  },
  methods: {
    showInput(e) {
      this.isVisible = e.target.checked;
    }
  }
};
</script>

