<template>
  <button v-on:click="store.changeTheme()"> Change Theme </button>
</template>

<script>
import store from '../store';

export default {
  name: 'Switcher',
  data: () => {
    return {
      store
    }
  }
}
</script>

<style scoped>
</style>
