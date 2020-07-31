<template>
  <div class="home">
    <div class="home--fixed">
      <TextInput v-on:convertString="convertString" :inputString.sync="text" />
    </div>
    <div class="home__wrapper">
      <CardList :inputString.sync="text" />
    </div>
  </div>
</template>

<script>
import TextInput from "../components/TextInput";
import CardList from "../components/CardList";
export default {
  name: "Home",
  components: {
    TextInput,
    CardList,
  },
  data() {
    return {
      text: "",
    };
  },
  methods: {
    convertString: function(stringText) {
      this.text = stringText;
    },
  },
};
</script>

<style lang="scss" scoped>
.home {
  &__wrapper {
    margin: 0 2em;
    padding-top: 200px;
  }

  &--fixed {
    position: fixed;
    width: 100%;
    top: 96px;
  }
}
</style>
