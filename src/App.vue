<template>
  <div id="app">
    <MyHeader/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'

export default {
  name: 'App',
  components: {
    MyHeader
}
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  border: 1px solid red;
}
</style>
