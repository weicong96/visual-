<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="scss">
html, body, #app ,#app>div{
  padding: 0;
  margin: 0;
  height: 100%;
  width: 100%;
}
</style>
