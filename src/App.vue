<template>
  <div class="container">
    <h1>Compare</h1>
    <Picker />
    <Picker />
  </div>
</template>

<script>
  import Picker from './components/Picker.vue'

  export default {
    components: {
      Picker
    }
  }
</script>

<style scoped>
html, body {
  height: 100%;
  width: 100%;
}
.container {
  width: 100%
}
</style>
