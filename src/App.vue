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
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  // border: 1px solid red;
}
.flex-row{
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}
.flex-col{
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
}
</style>
