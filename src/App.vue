<template>
  <div id="app">
    <div id="nav">
      <!-- NAVBAR -->
      <NavBar />
      <div :style="{ 'margin-left': sidebarWidth }">
        <router-view/>
      </div>
    </div>
  </div>
</template>

<style>
/* Color Palette */
:root {
  --softColor: #FDD8D4;
  --yellow: #f9a734;
  --DarkYellow: #fb8b24;
  --green: #36964c;
  --DarkGreen: #286e38;
}

/* Background pineapple styles , thanks to Angela Velasquez for the background https://codepen.io/AngelaVelasquez/pen/yVEOpY*/

body {
  background: /* Pineapple details */ radial-gradient(
      circle closest-side at 50px 50px,
      #fb8b24 3px,
      transparent 0
    ),
    radial-gradient(
      circle closest-side at 40px 60px,
      #fb8b24 3px,
      transparent 0
    ),
    radial-gradient(
      circle closest-side at 60px 60px,
      #fb8b24 3px,
      transparent 0
    ),
    radial-gradient(
      circle closest-side at 50px 70px,
      #fb8b24 3px,
      transparent 0
    ),
    radial-gradient(
      circle closest-side at 150px 165px,
      #fb8b24 3px,
      transparent 0
    ),
    radial-gradient(
      circle closest-side at 140px 175px,
      #fb8b24 3px,
      transparent 0
    ),
    radial-gradient(
      circle closest-side at 160px 175px,
      #fb8b24 3px,
      transparent 0
    ),
    radial-gradient(
      circle closest-side at 150px 185px,
      #fb8b24 3px,
      transparent 0
    ),
    /* Pineapple base */
      radial-gradient(
        ellipse closest-side at 50px 60px,
        #f9a734,
        18px,
        transparent 0
      ),
    radial-gradient(
      ellipse closest-side at 150px 175px,
      #f9a734,
      18px,
      transparent 0
    ),
    /* Pineapple leafs */
      radial-gradient(
        circle closest-side at 30px 40px,
        #FDD8D4 15px,
        transparent 0
      ),
    radial-gradient(
      circle closest-side at 40px 35px,
      #36964c,
      15px,
      transparent 0
    ),
    radial-gradient(
      circle closest-side at 70px 40px,
      #FDD8D4 15px,
      transparent 0
    ),
    radial-gradient(
      circle closest-side at 60px 35px,
      #286e38 15px,
      transparent 0
    ),
    radial-gradient(
      circle closest-side at 130px 155px,
      #FDD8D4 15px,
      transparent 0
    ),
    radial-gradient(
      circle closest-side at 140px 150px,
      #36964c,
      15px,
      transparent 0
    ),
    radial-gradient(circle at 170px 155px, #FDD8D4 15px, transparent 0),
    radial-gradient(circle at 160px 150px, #286e38 15px, transparent 0);
  background-color: var(--softColor);
  background-size: 180px 210px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>

<script>
import NavBar from './components/NavBar.vue'
import { sidebarWidth } from './javascript/state'

export default {
  name: 'App',
  components: {
    NavBar
  },
  setup () {
    return { sidebarWidth }
  }
}
</script>
