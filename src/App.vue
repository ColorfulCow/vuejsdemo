<template>
  <div id="app">
    <img class="logo" src="./assets/logo.png">
    <v-hello></v-hello>
    <input v-model="parentMsg">
    <v-header v-bind:my-message="parentMsg"></v-header>
  </div>
</template>

<script>
import VHello from './components/Hello'
import VHeader from './components/Header'
export default {
  components: {
    VHello,
    VHeader
  }
}
</script>

<style>
html {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

#app {
  margin-top: -100px;
  max-width: 600px;
  font-family: Helvetica, sans-serif;
  text-align: center;
}

.logo {
  width: 100px;
  height: 100px
}
</style>
