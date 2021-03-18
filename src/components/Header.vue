<template>
  <header>
    <h1>{{ title }} cheatsheet</h1>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    title: String
  }
}
</script>

<style scoped>
header {
  display: flex;
  border: 1px solid gray;
  padding: 20px;
}
</style>
