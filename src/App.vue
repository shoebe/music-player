<template>
  <ThePlaylistList/>
  <TheSongControl />
</template>

<script>
import TheSongControl from './components/playlist/TheSongControl.vue';
import ThePlaylistList from './components/playlist/ThePlaylistList.vue';

export default {
  name: 'App',
  components: {
    TheSongControl,
    ThePlaylistList
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
