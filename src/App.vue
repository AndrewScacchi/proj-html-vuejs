<template>
  <div id="app">
    <MyHeader/>
    <MyMain/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain

}
}
</script>
<style lang="scss">

@import "./assets/css/style.scss";

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}
#app {
  position:relative;
  scroll-margin-top: 100px;
}
 








</style>
