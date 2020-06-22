<template>
  <div class="col-md-4">
    <template v-for="(answer, i) in answers">
      <div v-if="answer.val" class="summary__item" :key="i">
        <h4>{{answer.title}}</h4>
        <span>{{answer.val}}</span>
      </div>
    </template>
  </div>
</template>

<script>
export default {
  name: "BriefSummary",
  props: ["answers"]
};
</script>