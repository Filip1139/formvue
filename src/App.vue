<template>
  <div class="container">
    <div class="row">
      <BriefQuestions @inputChange="setInput" />
      <BriefSummary :answers="answers" />
    </div>
  </div>
</template>

<script>
import BriefQuestions from "./components/BriefQuestions";
import BriefSummary from "./components/BriefSummary";

export default {
  name: "App",
  data() {
    return {
      answers: {
        haveSite: { val: "", title: "Strony www" },
        siteContent: { val: "", title: "Content" },
        siteRange: { val: "", title: "Zasięg" },
        haveBlog: { val: "", title: "Blog" }
      }
    };
  },
  components: {
    BriefQuestions,
    BriefSummary
  },
  methods: {
    setInput(e) {
      console.log(e.target.value);
      this.answers[e.target.name].val = e.target.value;
    }
  }
};
</script>

<style lang="scss">
</style>