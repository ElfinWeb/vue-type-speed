<template>
  <div class="container">
    <the-text-box :word="word">
      <the-score></the-score>
      <the-input></the-input>
    </the-text-box>
  </div>
</template>

<script>
import TheTextBox from "./components/TheTextBox.vue";
import TheScore from "./components/TheScore.vue";
import TheInput from "./components/TheInput.vue";
export default {
  name: "App",
  components: {
    TheTextBox,
    TheScore,
    TheInput,
  },
  data() {
    return {
      word: "",
    };
  },
  computed: {},
  methods: {
    randomWord() {
      fetch("https://random-word-api.herokuapp.com/word", {
        method: "GET",
      })
        .then((response) => response.json())
        .then((response) => {
          this.word = response[0];
        })
        .catch((err) => console.error(err));
    },
  },
};
</script>

<style>
* {
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
}

body {
  margin: 0;
  padding: 0;
}

.container {
  display: flex;
  margin: 0 auto;
  height: 100vh;
  align-items: center;
  background-image: url("./assets/pexels-min-an-1448709.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
