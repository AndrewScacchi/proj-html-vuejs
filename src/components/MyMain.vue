<template>
  <main id="main">
    <MyJumboTron/>
    <ContactUs/>
  </main>
</template>

<script>
import MyJumboTron from './minor/MyJumboTron.vue';
import ContactUs from './minor/ContactUs.vue';
export default {
  name: 'MyMain',
  components: {
    MyJumboTron,
    ContactUs
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