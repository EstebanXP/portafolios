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
      <NavBarLinks to="/about" icon="fas fa-columns">About</NavBarLinks>

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
  --sidebar-bg-color: #a1b434;
  --sidebar-item-hober: #38a169;
  --sidebar-item-active: #276749;
}
</style>

<style scoped>
.sidebar{
  color: white;
  background-color: var(--sidebar-bg-color);

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
