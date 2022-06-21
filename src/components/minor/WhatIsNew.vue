l<template>
<!-- creating a Jumbotron with img and file in flex -->
  <div id="OurClasses" class="flex-col">


    <div class="title flex-col">
      <h1>What is New</h1>
      <h4>Keep up to date with the latest news</h4>
      <img src="../../assets/images/header_divider.png" alt="">

    </div>
    <section class="flex-col main-a"> 
        <!-- cards container -->
        <div class="cardContainer flex-row">
             <!-- card -->
            <div class="card flex-col">
                <span>October 3, 2014</span>
                <div class="cardImg">
                    <img src="../../assets/images/blog_09.jpg" alt="">
                    <div class="absoluteBtn">42</div>
                </div>
                <div class="cardText">
                    <h3>Drawing and Painting Lessons</h3>
                    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Velit eius eum, impedit porro provident laudantium est dolorem. In beatae ad, laboriosam consequatur ab minus [..]</p>
                </div>
                <div class="cardFooter flex-row">
                    <div class="cardFooterItem flex-row">
                        <img src="../../assets/images/author.png" alt="">
                        <span>Anna Brown</span>
                    </div>
                    <div class="cardFooterItem flex-row">
                        <img src="../../assets/images/category.png" alt="">
                        <span>Events, Fun</span>
                    </div>

                </div>
            </div>
            <!-- card -->
            <div class="card flex-col">
                <span>October 3, 2014</span>
                <div class="cardImg">
                    <img src="../../assets/images/blog_10.jpg" alt="">
                    <div class="absoluteBtn">19</div>
                </div>
                <div class="cardText">
                    <h3>Fall Parents Meeting Day</h3>
                    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Velit eius eum, impedit porro provident laudantium est dolorem. In beatae ad, laboriosam consequatur ab minus [..]</p>
                </div>
                <div class="cardFooter flex-row">
                    <div class="cardFooterItem flex-row">
                        <img src="../../assets/images/author.png" alt="">
                        <span>Anna Brown</span>
                    </div>
                    <div class="cardFooterItem flex-row">
                        <img src="../../assets/images/category.png" alt="">
                        <span>Dance, Education</span>
                    </div>

                </div>
            </div>
             <!-- card -->
            <div class="card flex-col">
                <span>October 3, 2014</span>
                <div class="cardImg">
                    <img src="../../assets/images/blog_09.jpg" alt="">
                    <div class="absoluteBtn">22</div>
                </div>
                <div class="cardText">
                    <h3>Birthday in Kindergartner</h3>
                    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Velit eius eum, impedit porro provident laudantium est dolorem. In beatae ad, laboriosam [..]</p>
                </div>
                <div class="cardFooter flex-row">
                    <div class="cardFooterItem flex-row">
                        <img src="../../assets/images/author.png" alt="">
                        <span>Name of Author</span>
                    </div>
                    <div class="cardFooterItem flex-row">
                        <img src="../../assets/images/category.png" alt="">
                        <span>Blabalb balblab</span>
                    </div>

                </div>
            </div>

        </div>
        <div class="btn btn-orange">
            GO TO BLOG >
        </div>
        
    </section>

    
    
    
    
  </div>
</template>

<script>
export default {
  name: 'WhatIsNew',
  
  
 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#OurClasses{
    width: 100%;
    margin: 0 auto;
    padding: 25px 0;
    align-items: center;
    justify-content: space-around;
    gap: 25px;
    .title{
        justify-content: center;
        align-items: center;
        img{
            margin: 20px auto;
        }
    }
    section{
        justify-content: center;
        align-items: center;
        width: 100%;
        padding: 25px 15%;
        gap: 5%;
        
        //debug
        min-height: 200px;
        background-color: white;
    }
}
.main-a {
        gap: 20px
    }
.main-b{
    background-color: #f5f5f5;
    padding: 50px 15%;
    gap: 0;

}
.cardContainer{
    // width: 50%;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 5px;
    margin-bottom: 25px;
}
.card {
    width: 30%;
    height: 400px;
    border: 1px solid red;
    gap: 10px;
    img {
        width: 100%;
    }

}
.cardImg{
    position:relative;
}
.cardFooter {
    justify-content: flex-start;
    align-items: center;
    gap: 10px;
    margin-top: auto;
    padding: 10px 0;
    border-top: 1px solid grey;
    
}
.cardFooterItem {
    justify-content: flex-start;
    align-items: center;
    font-size: 0.8em;
    img {
    width: 15px;
    margin-right: 10px;
    }
}

.absoluteBtn {
        position: absolute;
        right: 0;
        bottom: 4px;
        z-index: 10;
        color: white;
        background-color: #fe6601;
        border:1px solid #fe6601;
        padding: 10px 15px;
        font-size: 1rem;
        font-weight: bold;

        &:hover {
            cursor: pointer;
            color: #fe6601;
            background-color: white;
        }
    
    }
</style>