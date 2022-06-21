<template>
<!-- just an img of a googleMaps prompt -->
<div id="imageGallery">
    <!-- static top 4 img -->
    <div class="imgGalleryTop ">
        <img src="../../assets/images/gallery_01.jpg" alt="">
        <img src="../../assets/images/gallery_02.jpg" alt="">
        <img src="../../assets/images/gallery_03.jpg" alt="">
        <img src="../../assets/images/gallery_04.jpg" alt="">
    </div>
    <div class="imgMain">
        <div class="blueBar flex-row">
            <h2>See Our Kindergarten Photo Gallery</h2>
            <div class="btn btn-blue">
                VIEW GALLERY >
            </div>
        </div>
        <!-- <img src="../../assets/images/parallax_02.jpg" alt=""> -->

    </div>
    <!-- bluebar -->
    <div>
        
    </div>
</div>
 
</template>

<script>
export default {
  name: 'ImageGallery',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

#imageGallery{
    width: 100%;
}
.imgGalleryTop{
    margin-bottom:-5px;
    img{
    width: 25%;
    }
} 
.imgMain{
    position: relative;
    height: 600px;
    background: url("../../assets/images/parallax_02.jpg");
    background-position: 0 -75px;
    background-size: cover;
    .blueBar{
        position: absolute;
        justify-content: space-between;
        padding: 0 15%;
        align-items: center;
        width:100%;
        height: 100px;
        top:0;
        left: 0;
        background: url("../../assets/images/pattern.png");
        h2{
            color: white;
        }
    }
    img{
        width:100%
    }
}

</style>