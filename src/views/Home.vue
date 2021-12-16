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
    <WhiteSpace inText="Hello World. Welcome to my Portfolio"></WhiteSpace>
  </div>
</template>

<script>
import WhiteSpace from '../components/WhiteSpace.vue'

export default {
  name: 'Home',
  components: {
    WhiteSpace
  }
}
</script>
