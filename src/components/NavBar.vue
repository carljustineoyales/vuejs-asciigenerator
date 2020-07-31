<template>
  <header>
    <nav class="nav">
      <div class="nav__appName">
        <h1>ASCII Art Generator</h1>
      </div>
      <ul class="nav__navList">
        <li class="nav__navItem">
          <router-link to="/vuejs-asciigenerator/" class="routerLink"
            >Home</router-link
          >
        </li>
        <li class="nav__navItem">
          <router-link to="/vuejs-asciigenerator/about" class="routerLink"
            >About</router-link
          >
        </li>
        <li class="nav__navItem">
          <a href="#" class="sourceLink"
            ><i class="fa fa-github-alt" aria-hidden="true"></i
          ></a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
import TextInput from "./TextInput";
export default {
  name: "NavBar",
};
</script>

<style lang="scss" scoped>
.nav {
  display: flex;
  padding: 2em;
  z-index: 999;
  position: fixed;
  width: 100%;
  background: #1b1b1b;
  top: 0;
  &__appName {
    flex: 1;
  }

  &__navList {
    display: flex;
  }

  &__navItem {
    display: flex;
    align-items: center;
    flex: 1;
    padding: 0 2em;

    .sourceLink {
      color: green;
      text-decoration: none;

      transition: all ease-in-out 0.3s;
      &:hover {
        color: white;
      }
      i {
        font-size: 28px;
      }
    }
    .routerLink {
      color: green;
      text-decoration: none;
      border-bottom: 1px solid transparent;
      transition: ease-in-out 0.3s;

      &:hover {
        color: green;
        border-color: green;
      }
    }
  }

  .router-link-exact-active {
    border-color: green;
  }
}
</style>
