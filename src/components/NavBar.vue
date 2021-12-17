<template>
    <div id="nav" class="sidebar" :style="{ width: sidebarWidth }">
      <h1>
          <span v-if="collapsed">
              <div>M</div>
              <div>P</div>
          </span>
          <span v-else>My Profile</span>
      </h1>

      <NavBarLinks to="/" icon="fas fa-home">Home</NavBarLinks>
      <NavBarLinks to="/about" icon="fas fa-user">About Me</NavBarLinks>
      <NavBarLinks to="/projects" icon="fas fa-folder-open">Projects</NavBarLinks>

      <span class="collapse-icon"
      :class="{ 'rotate-180': collapsed }"
      @click="toggleSidebar"
      >
       <i class="fas fa-angle-double-left" />
      </span>
      <br />
    </div>
</template>

<script>
import { collapsed, toggleSidebar, sidebarWidth } from '../javascript/state'
import NavBarLinks from '../components/NavBarLinks.vue'

export default {
  name: 'NavBar',
  props: {},
  components: { NavBarLinks },
  setup () {
    return { collapsed, toggleSidebar, sidebarWidth }
  }
}
</script>

<style>
:root{
  /**Color de el navbar */
  --sidebar-bg-color: #242121;
  /**Color del hover */
  --sidebar-item-hover: #534d4d;
  /**Color de el hover cuando haces click */
  --sidebar-item-active: #ff0000;
}
</style>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@1,200&display=swap');
.sidebar{
  color: white;
  background-color: var(--sidebar-bg-color);
  font-family: 'Poppins', sans-serif;

  float: left;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  bottom: 0;
  padding: 0.5em;

  transition: 0.3s ease;

  display: flex;
  flex-direction: column;
}

.sidebar h1 {
  height: 2.5em;
}

.collapse-icon {
    position: absolute;
    top: 0;
    padding: 0.75em;

    color: rgba(255, 255, 255, 0.7);
    transition: 0.2s linear;
}

.rotate-180 {
    transform: rotate(180deg);
    transition: 0.2s linear;
}
</style>
