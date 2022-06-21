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
        
        <!-- static quote -->
        <!-- <div  class="quote flex-col display-none">
            <div class="quote-wrapper flex-col">
                <img src="../../assets/images/quote_alt.png" alt="">
            </div>

            <p>I have to say that i have 2 children ages 5 and 2 and have used various daycare's in Kindergartens and this is by far the best i have ever used</p>
            <span class="line"></span>
            <span>Cecil J. Kirk</span>
        </div> -->

        <!-- :src="imgGallery[activeImg].img" -->
        <!-- dinamic quote -->
        <div id="quote" class="quote flex-col " @click="nextQuote">
            <div class="quote-wrapper flex-col">
                <img src="../../assets/images/quote_alt.png" alt="">
            </div>
            <p>{{quoteList[activeQuote].quoteText}}</p>
            <span class="line"></span>
            <span>{{quoteList[activeQuote].quoteAuthor}}</span>

            

        </div>
        <div class="bottom flex-row">
                <div v-for="(item, i) in quoteList" :key="i" class="rectangle"></div>

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
        activeQuote: 0,
        quoteList: [
            {
                quoteText: "I have to say that i have 2 children ages 5 and 2 and have used various daycare's in Kindergartens and this is by far the best i have ever used",
                quoteAuthor: "Cecil J. Kirk",
                // visible: false,
            },
            {
                quoteText: "If you are not yelling at your kids, you are not spending enought time with them",
                quoteAuthor: "Reese Whiterspoon",
                // visible: false,
            },
            
            {
                quoteText: "Do or do not. There is no try",
                quoteAuthor: "Jedi Master Yoda",
                // visible: false,
            },
            {
                quoteText: "This conversation has taken a turn for the moronic..",
                quoteAuthor: "Dorian Pavus",
                // visible: false,
            },
            {
                quoteText: "Se hai paura di ingrassare, fai a meno di mangiare, non pensare a me mangerò per tre.. finche l'appetito c'è!",
                quoteAuthor: "Asterix",
                // visible: false,
            },
            {
                quoteText: "If everything seems to be going well, you have obviously overlooked something.",
                quoteAuthor: "from Murphy's Laws",
                // visible: false,
            },
            
            
        ],
        // i wanna try change the background url..not sure how
        parallaxImgs : [
            {
                img: require("../../assets/images/parallax_02.jpg"),
            },
            {
                img: require("../../assets/images/parallax_01.jpg"),
            },
        ]
    }
   
  },
  methods: {
    nextQuote(){
                this.activeQuote++;
                if(this.activeQuote > this.quoteList.length - 1){
                    this.activeQuote = 0;
                    
                } 
                
            },
  }
   
}
//basic timing function
setInterval(() => {
    document.getElementById("quote").click();
}, 5000);
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
.display-none {
    display: none;
}

.bottom {
    position: absolute;
    bottom: 50px;
    width: 100%;
    justify-content: center;
    gap: 10px;
}
.rectangle {
    width: 40px;
    height: 12px;
    border: 2px solid $white;
}
.rectangle-up {
    bottom: 80px;
}

</style>