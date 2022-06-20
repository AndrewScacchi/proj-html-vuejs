<template>
  <main id="main">
    <MyJumboTron/>
    <WelcomeToFable/>
    <OurClasses/>
    <GoogleMap/>
    <ContactUs/>
  </main>
</template>

<script>
import MyJumboTron from './minor/MyJumboTron.vue';
import WelcomeToFable from './minor/WelcomeToFable.vue';
import OurClasses from './minor/OurClasses.vue';
import GoogleMap from './minor/GoogleMap.vue';
import ContactUs from './minor/ContactUs.vue';


export default {
  name: 'MyMain',
  components: {
    MyJumboTron,
    WelcomeToFable,
    OurClasses,
    GoogleMap,
    ContactUs,
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