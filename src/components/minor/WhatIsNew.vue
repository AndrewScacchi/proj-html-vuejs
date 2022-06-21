l<template>
<!-- creating a Jumbotron with img and file in flex -->
  <div id="whatIsNew" class="flex-col">


    <div class="title flex-col">
      <h1>What is New</h1>
      <h4>Keep up to date with the latest news</h4>
      <img src="../../assets/images/header_divider.png" alt="">

    </div>
    <section class="flex-col main-a"> 
        <!-- cards container -->
        <div class="cardContainer flex-row">
           
             <!-- dinamic card -->
            <div v-for="(post, i) in blogPosts" :key="i" class="card flex-col">
                <span>{{post.postDate}}</span>
                <div class="cardImg">
                    <img :src="post.postImg" :alt="post.postTitle">
                    <div class="absoluteBtn">{{post.postReply}}</div>
                </div>
                <div class="cardText">
                    <h3>{{post.postTitle}}</h3>
                    <p>{{post.postText}}</p>
                </div>
                <div class="cardFooter flex-row">
                    <div class="cardFooterItem flex-row">
                        <img src="../../assets/images/author.png" alt="">
                        <span>{{post.postAuthor}}</span>
                    </div>
                    <div class="cardFooterItem flex-row">
                        <img src="../../assets/images/category.png" alt="">
                        <span>{{post.postCategory}}</span>
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
  data(){
    return{
        blogPosts: [
            {
                postDate: "October 3, 2014",
                postImg: require("../../assets/images/blog_09.jpg"),
                postReply: "42",
                postTitle: "Drawing and Painting Lessons",
                postText: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Velit eius eum, impedit porro provident laudantium est dolorem. In beatae ad, laboriosam consequatur ab minus [..]",
                postAuthor: "Anna Brown",
                postCategory: "Dance, Education",

            },
            {
                postDate: "October 3, 2014",
                postImg: require("../../assets/images/blog_10.jpg"),
                postReply: "19",
                postTitle: "Fall Parents Meeting Day",
                postText: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Velit eius eum, impedit porro provident laudantium est dolorem. In beatae ad, laboriosam consequatur ab minus [..]",
                postAuthor: "Anna Brown",
                postCategory: "Events, Fun",

            },
            {
                postDate: "September 20, 2014",
                postImg: require("../../assets/images/blog_08.jpg"),
                postReply: "22",
                postTitle: "Birthday in KinderGartner",
                postText: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Velit eius eum, impedit porro provident laudantium est dolorem. In beatae ad, laboriosam consequatur ab minus [..]",
                postAuthor: "Anna Brown",
                postCategory: "Events, Fun",

            },
        ]
    }
  }
  
  
 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/css/style.scss";

#whatIsNew{
    @include main-id-style;
    
    
    section{
        justify-content: center;
        align-items: center;
        width: 100%;
        padding: 25px 15%;
        gap: 5%;
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
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 5px;
    margin-bottom: 25px;
}
.card {
    width: 30%;
    height: 400px;
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

</style>