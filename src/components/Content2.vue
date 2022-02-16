<template>
<div>
  <h2>나는 2번입니다</h2>
  <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam reiciendis tempore aut quibusdam ratione optio autem provident dolore? Ipsum, quidem! Esse id nihil officiis tempore expedita suscipit tempora tenetur vero!</p>
  <button v-on:click="proceed">Not interested.</button>
  <button v-on:click="proceed">More Information</button>
</div>
</template>

<script>
export default {
  emits: ['proceed-survey'],
  methods: {
    proceed() {
      this.$emit('proceed-survey')
    }
  }
}
</script>

<style>

</style>