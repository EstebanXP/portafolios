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
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@1,200&family=Raleway&display=swap');
/* Color Palette #FDD8D4*/
:root {
  --softColor: #d37166;
  --yellow: #f9a734;
  --DarkYellow: #fb8b24;
  --green: #36964c;
  --DarkGreen: #286e38;
}

body {
  background-color: whitesmoke;
  background-attachment: fixed;
}

#app {
  font-family: 'Raleway', sans-serif;
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
  color: #ffffff;
}

#nav a.router-link-exact-active {
  color: #ffffff;
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
