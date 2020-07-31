<template>
  <div class="asciiInput">
    <textarea @keyup="convertString" placeholder="type here ..."></textarea>
  </div>
</template>

<script>
export default {
  name: "TextInput",
  data() {
    return {
      text: "",
    };
  },
  props: {
    inputString: String,
  },

  methods: {
    convertString: function(event) {
      this.text = event.target.value;
      this.$emit("convertString", this.text);
    },
  },
};
</script>

<style lang="scss" scoped>
textarea {
  width: 100%;
  min-height: 40px;
  border: none;
  outline: none;
  background: none;
  caret-color: green;
  color: green;
  font-size: 30px;
  background: #1f1f1f;
  resize: vertical;
  padding: 0.5em;
  margin: auto;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
</style>
