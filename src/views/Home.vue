<template>
  <div class="home">
    <header>
      <h1>
        <strong>
          Hello world.
          Welcome to my Portfolio.
        </strong>
      </h1>
    </header>
    <WhiteSpace v-bind:inText='text'></WhiteSpace>
  </div>
</template>

<script>
import WhiteSpace from '../components/WhiteSpace.vue'

export default {
  name: 'Home',
  data () {
    return {
      text: 'Prueba'
    }
  },
  components: {
    WhiteSpace
  }
}
</script>
