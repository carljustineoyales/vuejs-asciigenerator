<template>
  <div id="app">
    <NavBar />
    <router-view />
  </div>
</template>

<script>
import NavBar from "./components/NavBar";
export default {
  name: "App",
  components: {
    NavBar,
  },
};
</script>

<style lang="scss">
@import url("./assets/css/style.scss");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html,
body {
  background: #1b1b1b;
  color: #fff;
  line-height: 1.4;
  // overflow-x: hidden;
  font-family: "DejaVuSansMono", Helvetica, sans-serif;

  ::-webkit-scrollbar {
    width: 10px;
  }
  ::-webkit-scrollbar-track {
    background: #f1f1f1;
  }

  /* Handle */
  ::-webkit-scrollbar-thumb {
    background: #888;
  }

  /* Handle on hover */
  ::-webkit-scrollbar-thumb:hover {
    background: #555;
  }
}

pre {
  color: green;
}
</style>
