<template>
  <div class="cardlist">
    <div class="cardlist__list">
      <div class="cardlist__items">
        <Card
          :inputString="inputString"
          :index="index"
          :importableFont="importableFont"
          v-for="(font, index) in importableFont"
          :key="index"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Card from "./Cards";
import { importableFont } from "../assets/fonts.js";
export default {
  name: "CardList",
  components: {
    Card,
  },
  data() {
    return {
      importableFont,
    };
  },
  props: {
    inputString: String,
  },
};
</script>

<style></style>
