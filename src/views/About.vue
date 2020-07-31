<template>
  <div class="about">
    <div class="about__wrapper">
      <div class="about__appName">
        <pre>
            _____  _____ _____ _____            _____ _______   
     /\    / ____|/ ____|_   _|_   _|     /\   |  __ \__   __|  
    /  \  | (___ | |      | |   | |      /  \  | |__) | | |     
   / /\ \  \___ \| |      | |   | |     / /\ \ |  _  /  | |     
  / ____ \ ____) | |____ _| |_ _| |_   / ____ \| | \ \  | |     
 /_/____\_\_____/ \_____|_____|_____| /_/  __\_\_| _\_\ |_|___  
  / ____|  ____| \ | |  ____|  __ \     /\|__   __/ __ \|  __ \ 
 | |  __| |__  |  \| | |__  | |__) |   /  \  | | | |  | | |__) |
 | | |_ |  __| | . ` |  __| |  _  /   / /\ \ | | | |  | |  _  / 
 | |__| | |____| |\  | |____| | \ \  / ____ \| | | |__| | | \ \ 
  \_____|______|_| \_|______|_|  \_\/_/    \_\_|  \____/|_|  \_\
                                                                
</pre
        >
        <div class="about__desc">
          <p>*This is a generated ascii art</p>
          <br /><br />
          <p>
            This app is created using
            <a href="https://vuejs.org/" target="_blank">Vuejs</a> and
            <a href="https://www.npmjs.com/package/figlet" target="_blank"
              >Figlet</a
            >
          </p>
          <p>Will add more fonts in the future update</p>
          <br /><br />

          <p>
            <a
              href="https://github.com/patorjk/figlet.js/tree/master/importable-fonts"
              target="_blank"
              >Click here</a
            >
            to see the available importable fonts in Figlet
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.about {
  &__desc {
    pre {
      display: inline;
    }
    a {
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

  &__wrapper {
    margin: 0 2em;
    padding-top: 100px;
  }
}
</style>
