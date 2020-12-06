<template>
  <div id="app">
    <header>
      <navbar/>
    </header>
  </div>
</template>

<script>
import navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components: {
    navbar
  }
}
</script>

<style>
*, ::before, ::after {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

a {
    text-transform: none;
    outline: none;
    text-decoration: none;
}

ul {
  list-style: none;
}

header {
  min-height: 100vh;
}
</style>
