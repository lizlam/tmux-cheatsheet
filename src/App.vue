<template>
  <Cheatsheet title="tmux" v-on:show-cheatsheet="show" />
  <div v-if="showBody">
    <Body />
  </div>
</template>

<script>
import Cheatsheet from './components/Cheatsheet'
import Body from './components/Body'

export default {
  name: 'App',
  components: {
    Cheatsheet,
    Body
  },
  data () {
    return {
      showBody: false
    }
  },
  methods: {
    show () {
      this.showBody = !this.showBody
    }
  },
  emits: ['show-cheatsheet']
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
