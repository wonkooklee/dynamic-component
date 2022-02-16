<template>
  <div id="app">
    <tap-view></tap-view>
  </div>
</template>

<script>
import TapView from './pages/TapView.vue'

export default {
  name: 'App',
  data() {
    return {
      currentView: 'home',
    }
  },
  components: {
    TapView
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400&display=swap');

body {
  font-family: 'Roboto', sans-serif;
}

h2 {
  margin: 30px 0;
}

p {
  font-size: 18px;
  font-weight: 300;
  line-height: 150%;
}

button {
  margin: 40px 10px 0 0;
  padding: 10px 25px;
  border: none;
  border-radius: 4px;
  color: #fff;
  background-color: dodgerblue;
  font-weight: 400;
  cursor: pointer;
}
</style>
