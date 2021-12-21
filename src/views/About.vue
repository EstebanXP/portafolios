<template>
  <div class="about">
    <h1>This is an about page, kind of.</h1>
    <br />
    <!--Primer input-->
    <h2>About me</h2>
    <WhiteSpace v-bind:inText="text"></WhiteSpace>
    <br />
    <div>
      <!--Segundo input-->
      <h2>Technical Skills</h2>
      <WhiteSpace v-bind:inText="text2"></WhiteSpace>
      <div class="sibling-fade">
        <a href="#">C</a>
        <a href="#">C++</a>
        <a href="#">NoSQL Database: Firebase</a>
        <a href="#">NoSQL Database: MongoDB</a>
        <a href="#">Java</a>
        <a href="#">JavaScript</a>
        <a href="#">JavaScript: React</a>
        <a href="#">JavaScript: Vue</a>
        <a href="#">SQL</a>
        <a href="#">OOP Conpcepts</a>
        <a href="#">CSS</a>
        <a href="#">Node.Js</a>
        <a href="#">Git</a>
        <a href="#">GitHub</a>
      </div>
    </div>
    <!--Tercer input-->
    <h2>Soft Skills</h2>
    <WhiteSpace v-bind:inText="text3"></WhiteSpace>
    <div class="sibling-fade">
        <a href="#">Intermediate spoken and written english level</a>
        <a href="#">Related to Scrum Methodology</a>
        <a href="#">Ready to meet new people and learn new abilities</a>
      </div>
    <br />
  </div>
</template>

<script>
import WhiteSpace from '../components/WhiteSpace.vue'
export default {
  name: 'About',
  data () {
    return {
      text: 'I am Esteban Xelhuantzi, i am 22 years old and currently on 9th semester of the Computer Science degree. ',
      text2: 'During my college time and by personal projects these are the technologies and concepts i learned, have minimum a basic level and usually use',
      text3: 'Technical Skills are important, but, i also have these skills '
    }
  },
  components: {
    WhiteSpace
  }
}
/**
 *<div>
        <ul>
          <li>C</li>
          <li>C++</li>
          <li>Java</li>
          <li>JavaScript</li>
          <ul>
            <li>Vue</li>
            <li>React</li>
          </ul>
          <li>SQL</li>
          <li>OOP Conpcepts</li>
          <li>NoSQL Database</li>
          <ul>
            <li>MongoDB</li>
            <li>Firebase</li>
          </ul>
          <li>CSS</li>
          <li>Node.js</li>
          <li>Git</li>
          <li>GitHub</li>
        </ul>
      </div> */
</script>

<style scoped>
html {
  display: flex;
}

body {
  padding: 10px;
  max-width: 40em;
  margin: auto;
}
/* SIBLING FADE: fade out siblings around a hovered item */

.sibling-fade { visibility: hidden; }
/* Prevents :hover from triggering in the gaps between items */

.sibling-fade > * { visibility: visible; }
/* Brings the child items back in, even though the parent is `hidden` */

.sibling-fade > * { transition: opacity 150ms linear 100ms, transform 150ms ease-in-out 100ms; }
/* Makes the fades smooth with a slight delay to prevent jumps as the mouse moves between items */

.sibling-fade:hover > * { opacity: 0.4; transform: scale(0.9); }
/* Fade out all items when the parent is hovered */

.sibling-fade > *:hover { opacity: 1; transform: scale(1); transition-delay: 0ms, 0ms; }
/* Fade in the currently hovered item */
.sibling-fade {
  background: #f05555;
  display: flex;
  flex-wrap: wrap;
  margin-left: 9.5%;
  margin-right: 9.5%;
}
.sibling-fade > * {
  background: black;
  padding: 1em;
  flex: auto;
  margin: 0.3em;
  text-align: center;
  color: #000000;
  font-size: 1.5em;
  text-decoration: none;
}
</style>
