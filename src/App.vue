<template>
  <div id="app">
    <theme-provider>
      <div class="hero">
        <h1>Change Theme!</h1>
        <switcher />
      </div>
    </theme-provider>
  </div>
</template>

<script>
import Switcher from './theme/Switcher.vue'
import ThemeProvider from './theme/ThemeProvider.vue'

export default {
  name: 'App',
  components: {
    ThemeProvider,
    Switcher
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@600&display=swap');

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.hero {
  background-color: var(--background);
  height: 100vh;
  width: 100vw;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  transition: all 0.3s ease-in-out;
}

.hero h1 {
  margin: 0 0 1rem;
  color: var(--text);
  font-family: 'Montserrat', sans-serif;
}
</style>
