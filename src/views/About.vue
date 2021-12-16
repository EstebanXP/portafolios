<template>
  <div class="about">
    <h1>This is an about page, kind of.</h1>
    <br>
    <h2>Hola mundo</h2>
    <WhiteSpace v-bind:inText='text'></WhiteSpace>
    <br>
    <h2>Hola mundo</h2>
    <WhiteSpace v-bind:inText='text2'></WhiteSpace>
  </div>
</template>

<script>
import WhiteSpace from '../components/WhiteSpace.vue'
export default {
  name: 'About',
  data () {
    return {
      text: 'PRUEBA asda adasdas',
      text2: 'asdasdasdasdasdasd'
    }
  },
  components: {
    WhiteSpace
  }
}
</script>
