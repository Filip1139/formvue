<template>
  <div class="md-8">
    <form>
      <QuestionItem
        :title="'1. Czy posiadają Państwo obecnie stronę internetową?'"
        @inputChange="inputChange"
      >
        <RadioText
          :name="'haveSite'"
          :id="'haveSite-1'"
          :value="'Posiadam strone'"
          :title="'tak'"
          :isChecked="questions"
        />
        <Radio :name="'haveSite'" :id="'haveSite-2'" :value="'Nie posiadam strony'" :title="'nie'" />
      </QuestionItem>

      <QuestionItem
        :title="'2. Czy kopiujemy wartość merytoryczną z obecnie istniejącej strony?'"
        @inputChange="inputChange"
      >
        <Radio
          :name="'siteContent'"
          :id="'content-all'"
          :value="'Kopiujemy całość wartość merytoryczną'"
          :title="'Całosć'"
        />
        <Radio
          :name="'siteContent'"
          :id="'content-part'"
          :value="'Kopiujemy część wartości merytorycznej'"
          :title="'Część'"
        />
        <Radio
          :name="'siteContent'"
          :id="'content-new'"
          :value="'Potrzebuje nowej wartości merytorycznej'"
          :title="'Nowa wartość merytoryczna'"
        />
      </QuestionItem>
      <QuestionItem :title="'3. Jaki ma być obszar zasięgu oferty?'" @inputChange="inputChange">
        <Radio
          :name="'siteRange'"
          :id="'range-local'"
          :value="'Kopiujemy całość wartość merytoryczną'"
          :title="'Całosć'"
        />
        <Radio
          :name="'siteRange'"
          :id="'range-country'"
          :value="'Kopiujemy część wartości merytorycznej'"
          :title="'Część'"
        />
        <Radio
          :name="'siteRange'"
          :id="'range-abroad'"
          :value="'Potrzebuje nowej wartości merytorycznej'"
          :title="'Nowa wartość merytoryczna'"
        />
      </QuestionItem>

      <QuestionItem
        :title="'5. Czy strona powinna posiadać zakładkę Blog?'"
        @inputChange="inputChange"
      >
        <Radio
          :name="'haveBlog'"
          :id="'site-blog-yes'"
          :value="'Chcę mieć na swojej nowej stronie zakładkę Blog'"
          :title="'Tak'"
        />
        <Radio
          :name="'haveBlog'"
          :id="'site-blog-no'"
          :value="'Nie chcę zakładki Blog'"
          :title="'Nie'"
        />
      </QuestionItem>

      <button type="submit" class="btn btn-primary">Submit</button>
    </form>
  </div>
</template>

<script>
import QuestionItem from "./QuestionItem";
import Radio from "./Radio";
import RadioText from "./RadioText";

export default {
  name: "BriefLeft",
  props: ["questions"],
  components: { QuestionItem, Radio, RadioText },
  methods: {
    inputChange(e) {
      this.$emit("inputChange", e);
    }
  }
};
</script>