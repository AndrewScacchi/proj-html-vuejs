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
    <!-- main image  -->
    <div class="imgMain">
        <div class="blueBar flex-row">
            <h2>See Our Kindergarten Photo Gallery</h2>
            <div class="btn btn-blue">
                VIEW GALLERY >
            </div>
        </div>
        
        <div class="quote flex-col">
            <div class="quote-wrapper flex-col">
                <img src="../../assets/images/quote_alt.png" alt="">
            </div>

            <p>I have to say that i have 2 children ages 5 and 2 and have used various daycare's in Kindergartens and this is by far the best i have ever used</p>
            <span class="line"></span>
            <span>Cecil J. Kirk</span>
        </div>

    </div>
    <!-- bluebar -->
    
</div>
 
</template>

<script>
export default {
  name: 'ImageGallery',

  data(){
    return{
        quoteList: [
            {
                quoteText: "placeholder1",
                quoteAuthor: "Author1",
                visible: false,
            },
            {
                quoteText: "placeholder2",
                quoteAuthor: "Author2",
                visible: false,
            },
            
            {
                quoteText: "placeholder3",
                quoteAuthor: "Author3",
                visible: false,
            },
            
            
        ],
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

@import "../../assets/css/style.scss";

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
    .quote {
        position:absolute;
        width:100%;
        height: calc(100% - 100px);
        bottom: 0;
        left: 0;
        color: $white;
        padding: 0 20%;
        text-align: center;

        justify-content: center;
        align-items: center;

        p {
            font-size: 2em;
            font-weight: lighter;
        }
        span.line {
            content: "";
            width: 50px;
            border-top: 1px solid $white;
            margin: 25px 0;
        }

        //debug
        border: 1px solid black;

    }
    .quote-wrapper{
        justify-content: center;
        align-items: center;
        padding: 20px;
        border-radius: 50%;
        border: 2px solid $white;
        margin-bottom: 25px;
    }
}


</style>