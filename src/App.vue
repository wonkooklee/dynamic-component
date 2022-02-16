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
