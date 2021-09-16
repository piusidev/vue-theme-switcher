<template>
  <div id="app" v-bind:theme="store.state.theme">
    <div>
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
</style>
