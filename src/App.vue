<template>
  <div id="app">
    <Header />
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="6" offset="3"><QuestionBox /></b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Header from "./components/Header";
import QuestionBox from "./components/QuestionBox";

export default {
  name: "App",
  components: {
    Header,
    QuestionBox,
  },
  data() {
    return {
      question: [],
    };
  },
  mounted: function() {
    fetch("https://opentdb.com/api.php?amount=10&category=27&type=multiple", {
      method: "get",
    })
      .then((res) => {
        return res.json();
      })
      .then((data) => {
        this.question = data.results;
        console.log(this.question, "tegas vue");
      });
  },
};
</script>
