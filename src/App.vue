<template>
  <div id="app" v-bind:theme="store.state.theme">
    <div class="hero">
      <h1>Change Theme!</h1>
      <switcher />
    </div>
  </div>
</template>

<script>
import Switcher from './components/Switcher.vue'
import store from './store'

export default {
  name: 'App',
  components: {
    Switcher
  },
  data: () => {
    return {
      store
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@600&display=swap');

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

#app[theme="dark"] {
  --background: #282a36;
  --text: #f8f8f2;
}

#app[theme="light"] {
  --background: #f8f8f2;
  --text: #282a36;
}

#app {
  background-color: var(--background);
  height: 100vh;
  width: 100vw;

  display: flex;
  align-items: center;
  justify-content: center;
}

.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.hero h1 {
  margin: 0 0 1rem;
  color: var(--text);
  font-family: 'Montserrat', sans-serif;
}
</style>
