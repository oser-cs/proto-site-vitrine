<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style lang="scss">
@import 'src/assets/scss/variables';
@import './assets/font-awesome/css/font-awesome.min.css';

body {
  margin: 0;
  font-family: $font-body;
  font-size: $font-size-regular;

  html {
    height: 100%;
  }
}
</style>
