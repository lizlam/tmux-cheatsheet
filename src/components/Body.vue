<template>
  <div class="container" v-on:keydown="handleToggle">
    <button v-on:click="handleToggle">
      <key>C-b %</key>
    </button>
    <div class="text">Split screen vertically</div>
    <div v-if="!toggleOn">
      <div class="screen"></div>
    </div>
    <div v-else class="screen-container">
      <div class="split-screen"></div>
      <div class="split-screen"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Body',
  data () {
    return {
      toggleOn: true
    }
  },
  methods: {
    handleToggle (e) {
      console.log(e)
      this.toggleOn = !this.toggleOn
    }
  }
}
</script>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 100px 300px 1fr;
}
button {
  height: 50px;
  width: 70px;
  padding: 10px;
  margin: 40px;
  border: 1px solid grey;
  border-radius: 3px;
  background: cornsilk;
}
button:hover {
  border: 2px solid darkgrey;
  background: wheat;
}
.text {
  margin: 52px;
}
.screen {
  height: 150px;
  width: 200px;
  background: black;
}
.screen-container {
  display: flex;
}
.split-screen {
  display: in-line;
  height: 150px;
  width: 100px;
  background: black;
  border-right: 1px solid white;
}
</style>
