<template>
  <div class="about">
    <h1>This is an about page, kind of.</h1>
    <br>
    <!--Primer input-->
    <h2>About me</h2>
    <WhiteSpace v-bind:inText='text'></WhiteSpace>
    <br>
    <!--Segundo input-->
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
      text: 'I am Esteban Xelhuantzi, i am 22 years old and currently on 9th semester of the Computer Science degree. ',
      text2: 'Photography and videogames are my hobbies'
    }
  },
  components: {
    WhiteSpace
  }
}
</script>
