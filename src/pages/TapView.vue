<template>
  <section>
    <ul>
      <li v-on:click="activeOnClick" v-bind:class="{active: currentSelection === 0}" id="0">1</li>
      <li v-on:click="activeOnClick" v-bind:class="{active: currentSelection === 1}" id="1">2</li>
      <li v-on:click="activeOnClick" v-bind:class="{active: currentSelection === 2}" id="2">3</li>
    </ul>
    <div class="content">
      <component @proceed-survey="proceedSurvey" v-bind:is="currentComponent[currentSelection]"></component>
    </div>
  </section>
</template>

<script>
import Content1 from '@/components/Content1.vue'
import Content2 from '@/components/Content2.vue'
import Content3 from '@/components/Content3.vue'

export default {
  data() {
    return {
      currentComponent: ['Content1', 'Content2', 'Content3'],
      currentSelection: 0
    }
  },
  components: {
    Content1, Content2, Content3
  },
  methods: {
    activeOnClick(e) {
      const { id } = e.target;
      this.currentSelection = parseInt(id)
    },
    proceedSurvey() {
      if (this.currentSelection !== 2) {
        this.currentSelection++
        return
      }
      this.currentSelection = 0
    }
  },
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
section {
  display: flex;
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
ul {
  list-style: none;
}
li {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 50px;
  height: 33%;
  font-size: 24px;
  background-color: #dedede;
  border-bottom: 1px solid black;
  cursor: pointer;
}
li:last-child {
  border-bottom: none;
}
.active {
  background-color: dodgerblue;
}
.content {
  padding: 30px;
  width: 700px;
  height: 400px;
  background-color: #f4f4f4;
  font-size: 24px;
}
</style>