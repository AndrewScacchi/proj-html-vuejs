<template>
<!-- building a bigger img from smallers -->
<div id="google-images">
    <img v-for="(image, i ) in googleMaps" :key="i" :src="image.img" alt="">

</div>
 
</template>

<script>
export default {
  name: 'GoogleMap',
  data(){
    return{
        googleMaps: [
            {
                text: "vt(1)",
                img: require("../../assets/img/googleMaps/vt (1).png"),
            },
            {
                img: require("../../assets/img/googleMaps/vt (2).png"),
            },
             {
                img: require("../../assets/img/googleMaps/vt (3).png"),
            },
            {
                img: require("../../assets/img/googleMaps/vt (4).png"),
            },
            
            
        ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

#google-images{
    width: 100%;
    height: 300px;
    background-color: grey;
}

</style>