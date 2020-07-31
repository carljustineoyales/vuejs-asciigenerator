<template>
  <div class="cards">
    <p>{{ fontName }}</p>
    <br />
    <div class="outputFigDisplay">
      <pre>{{ generatedString }}</pre>
    </div>
  </div>
</template>

<script>
import figlet from "figlet";

export default {
  name: "Cards",
  data() {
    return {
      generatedString: "",
      fontName: this.importableFont[this.index].fontname,
    };
  },
  props: {
    inputString: String,
    index: Number,
    importableFont: Array,
  },
  mounted() {
    this.convert();
  },

  watch: {
    inputString: function(newValue) {
      this.convert();
    },
  },
  methods: {
    convert: function() {
      figlet.parseFont(
        this.importableFont[this.index].fontname,
        this.importableFont[this.index].asciiFont
      );

      figlet.text(
        this.inputString,
        {
          font: this.importableFont[this.index].fontname,
        },
        function(err, data) {
          this.convertText(data);
        }.bind(this)
      );
    },
    convertText(data) {
      this.generatedString = data;
    },
  },
};
</script>

<style lang="scss" scoped>
.cards {
  overflow: hidden;
  margin: 2em 0;
  padding: 2em;
  min-height: 100px;
  border: 1px white solid;
}
</style>
