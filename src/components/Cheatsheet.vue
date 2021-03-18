<template>
  <Header v-bind:title="title" />
  <button v-on:click="onClick(title)">Show</button>
</template>

<script>
import Header from './Header'

export default {
  name: 'Cheatsheet',
  props: {
    title: String
  },
  components: {
    Header
  },
  methods: {
    onClick (t) {
      console.log(t)
      this.$emit('show-cheatsheet', t)
    }
  }
}
</script>
