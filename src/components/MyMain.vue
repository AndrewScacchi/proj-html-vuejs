<template>
  <main id="main">
    <MyJumboTron/>
    
  </main>
</template>

<script>
import MyJumboTron from './minor/MyJumboTron.vue';
export default {
  name: 'MyMain',
  components: {
    MyJumboTron
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#main{
  // background-color: aquamarine;
  min-height: calc(100vh - 100px);
}

</style>