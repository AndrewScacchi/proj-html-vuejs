<template>
<!-- creating a Jumbotron with img and file in flex -->
  <div id="welcomeToFable" class="flex-col">


    <div class="title flex-col">
      <h1>Welcome to Fable</h1>
      <h4>Our contact adress and contact details</h4>
      <img src="../../assets/images/header_divider.png" alt="">

    </div>
    <section class="flex-row main-a">
        <!-- statyc cards -->
        <div class="card">
            <div class="round round-orange">
                <img src="../../assets/images/schoolbag_alt.png" alt="">
            </div>
            <h3>Morbi Etos</h3>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.  at laudantium asperiores nisi</p>
        </div>
        <div class="card">
            <div class="round round-blue">
                <img src="../../assets/images/stroller_alt.png" alt="">
            </div>
            <h3>Congue Gravidas</h3>
            <p> Ipsum fuga rerum corrupti, odit aspernatur illum harum fugiat illo at laudantium asperiores nisi</p>
        </div>
        <div class="card">
            <div class="round round-orange">
                <img src="../../assets/images/globe_alt.png" alt="">
            </div>
            <h3>Maecenas Node</h3>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum fuga rerum corrupti,laudantium asperiores nisi</p>
        </div>
        <div class="card">
            <div class="round round-blue">
                <img src="../../assets/images/bell_alt.png" alt="">
            </div>
            <h3>Praesent Morbi</h3>
            <p>Ipsum fuga rerum corrupti, odit aspernatur illum harum fugiat illo at laudantium asperiores nisi</p>
        </div>
    
    </section>
    <section class="main-b">
        <div class="section-container flex-row">
            <!-- left div -->
            <div class="section-left flex-col">
                <div class="left-icon flex-row">
                    <div class="btn btn-orange">Overwiew</div>
                    <div class="btn btn-white" >Our Mission</div>
                </div>
                <h2 class="left-title">Our philosphy is learning through play as we offer a stimulating enviroment for children. </h2>
                <!-- small cards -->
                <div class="left-smallCards"> 
                    <div class="smallCard flex-row">
                        <div class="smallCard-img">
                            <img src="../../assets/images/clock_alt.png" alt="">
                        </div>
                        <div class="smallCard-text">                       
                            <h3>Full Day Sessions</h3>
                            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Doloremque tempore dicta blanditiis pariatur, amet.</p>
                        </div>

                    </div>
                    
                    <div class="smallCard flex-row">
                        <div class="smallCard-img">
                            <img src="../../assets/images/diagram_alt.png" alt="">
                        </div>
                        <div class="smallCard-text">                       
                            <h3>Varied Classes</h3>
                            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Doloremque tempore dicta blanditiis pariatur, amet.</p>
                        </div>
                    </div>
                </div>
                
                

            </div>
            <!-- right div -->
            <div class="section-right flex-col">
                <div class="img-main">
                    <img :src="imgGallery[activeImg].img" alt="">
                    <!-- <img src="../../assets/images/gallery_08-690x506.jpg" alt=""> -->
                    <div class="btn btn-orange left" @click="prevImg" id="prev">&lt;</div>
                    <div class="btn btn-orange right" @click="nextImg" id="next">></div>
                </div>
                <!-- gallery at the bottom -->
                <div class="img-gallery flex-row">
                    <img class="bottomBorder" v-for="(img, i) in imgGallery" :key="i" :src="img.img" alt="" :class="i === activeImg ? 'bottomBorderActive' : '' " >
                </div>
                
            </div>
            
        </div>

    </section>
    
    
    
    
  </div>
</template>

<script>
export default {
  name: 'WelcomeToFable',
    data(){
        return{
            activeImg: 0,
            imgGallery: [
                {
                   img: require("../../assets/images/gallery_07-690x506.jpg"),
                   isActive: false, 
                },
                {
                   img: require("../../assets/images/gallery_01-690x506.jpg"),
                   isActive: false, 
                },
                {
                   img: require("../../assets/images/gallery_08-690x506.jpg"),
                   isActive: false, 
                },

            ]
        }
    },
    methods : {
            nextImg(){
                this.activeImg++;
                if(this.activeImg > this.imgGallery.length - 1){
                    this.activeImg = 0;
                
                } 
                
            },
            prevImg(){
                this.activeImg--;
                if(this.activeImg < 0 ){
                    this.activeImg = this.imgGallery.length - 1;
                    
                }
            },
            
    }
   
}

//basic timing function
setInterval(() => {
    document.getElementById("next").click();
}, 3000);
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/css/style.scss";

#welcomeToFable{
    @include main-id-style;
  section{
    justify-content: center;
    align-items: center;
    width: 100%;
    padding: 25px 15%;
    gap: 5%;
    .section-container {
        width: 100%;
        padding: 0 15%;
        
        .section-left, .section-right{         
            width: 50%;
        }
        .section-left {
            padding: 20px ;
            gap: 20px;
            justify-content: space-between;

        }
        .section-right {
            gap: 10px;
        }
    }
    .card{
    
    width: 15%;
    justify-content: center;
    align-items: center;
    text-align: center;
    img{
      height: 60px;
    }
    h3 {
      margin: 10px 0;
      font-weight: bold;
    }
    p {
      font-size: 0.8rem;
    }
    }
  }
  .main-b{
    padding: 25px;
    background-color: $darkWhite;
  }
  
}
.round{
        border-radius: 50%;
        height: 150px;
        width: 150px; 
        display: flex;
        align-items: center;
        justify-content: center;

        &-orange{
            background-color: #fe6601;
        }
        &-blue{
            background-color: #56509f;
        }
        
    }

.smallCard {
    margin: 10px auto;
    justify-content: center;
    align-items: center;
    gap: 10px;
    .smallCard-img{
        background: $blazeOrange;
        border-radius: 50%;
        padding: 15px;
        display: flex;
        align-items: center;
        justify-content: center;
    
    }
}
.img-gallery {
    justify-content: space-between;
    img{
        width: 32%;
    }
}
.img-main{
    position: relative;
    img{
        width: 100%;
    }
    div.btn{
        position: absolute;
        width:40px;
        height: 40px;
        text-align: center;
        line-height: 40px;
        padding: 0;
        font-weight: bold;
        font-size: 20px;
    }
    .left{
        left: 0;
        bottom: 50%;
    }
    .right {
        right: 0;
        bottom: 50%;
    }
}
.btn-white {
    margin-left: 10px;
}
// this class should be given on the active element..
.bottomBorder {
    border-bottom: 2px solid $darkWhite;
    padding-bottom: 10px
}
.bottomBorderActive {
    border-bottom: 2px solid $blazeOrange;
    padding-bottom: 10px
}
</style>