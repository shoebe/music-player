<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <TheSongControl />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TheSongControl from './components/playlist/TheSongControl.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    TheSongControl
  }
}
</script>

<style>
:root {
  --bg-colour: #95274F;
  --light-colour: #D38383;
  --dark-colour: #641B36;
  --dark-shadow-colour: #641B3650;
}

#app {
  font-family: 'Spartan';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: var(--light-colour);
}
</style>
