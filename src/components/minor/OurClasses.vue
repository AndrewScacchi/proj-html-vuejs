l<template>
<!-- creating a Jumbotron with img and file in flex -->
  <div id="OurClasses" class="flex-col">


    <div class="title flex-col">
      <h1>Our Classes</h1>
      <h4>Our preschool program has four dedicated classes</h4>
      <img src="../../assets/images/header_divider.png" alt="">

    </div>
    <section class="flex-col main-a">
        <!-- section title card -->
        <div class="section-title flex-row">
            <h2>
                We provide four classes with nine to twenty children each aged twelve months to five years of ages.
            </h2>
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem ipsa doloribus quod sequi incidunt quidem officia quas. Quos reiciendis accusamus aperiam maiores libero iste sit aut aliquam, ipsam magnam laudantium.
            </p>
            
        </div>
        <!-- cards container -->
        <div class="classContainer flex-row">
            <!-- Dynamic card -->
            <div v-for="(classe, i) in classesList" :key="i" class="classCard flex-row">
                <!-- card text -->
                <div class="classCard-text flex-col">
                    <div class="className">
                        <h3>{{classe.className}}</h3>
                        <p>Class name</p>
                    </div>
                    <div class="classStats flex-row">
                        <div class="classStats-1 flex-col">
                            <span>{{classe.ageRange}}</span>
                            <span class="minor">{{classe.ageRangeName}}</span>
                        </div>
                        <div class="classStats-2 flex-col">
                            <span>{{classe.classSize}}</span>
                            <span class="minor">Class Size</span>
                        </div>
                    </div>                    
                </div>
                <!-- card img -->
                <img class="classCard-img" :src="classe.img" :alt="classe.className">
                <!-- card btn -->
                <div class="absoluteBtn">
                    READ MORE >
                </div>

            </div>    
        </div>
    </section>
    <section class="main-b flex-row">
        <div class="left">
            <h2>We have been educating children for over fifteen years. Our goal is to create a place that engages each child.</h2>
            <p> Molestias consequatur iure culpa voluptatem voluptatum id dignissimos ea maiores, magnam, cum quas excepturi aliquam inventore dolore in quis necessitatibus facilis ratione?</p>

            <ul>
                <li>Comprehensive reporting on individual achievements</li>
                <li>
                    Educational field trips and school presentations
                </li>
                <li>
                    Individual attention in a small-class setting
                </li>
                <li>
                    Learning program with after-school care
                </li>
                <li>
                    Opportunities to carry out scientific investigations
                </li>
                <li>
                    Positive learning eniviroment for your child
                </li>
            </ul>

        </div>
        <div class="cardContainer flex-row">
            <div class="card flex-col">
                <div class="round round-white">
                    <img src="../../assets/images/school.png" alt="">
                </div>
                <h3>Frendly Place</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. </p>
            </div>
            <div class="card flex-col">
                <div class="round round-white">
                    <img src="../../assets/images/school.png" alt="">
                </div>
                <h3>Frendly Place</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. </p>
            </div>
            <div class="card flex-col">
                <div class="round round-white">
                    <img src="../../assets/images/school.png" alt="">
                </div>
                <h3>Frendly Place</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. </p>
            </div>
            <div class="card flex-col">
                <div class="round round-white">
                    <img src="../../assets/images/school.png" alt="">
                </div>
                <h3>Frendly Place</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. </p>
            </div>

        </div>
        

    </section>
    
    
    
    
  </div>
</template>

<script>
export default {
  name: 'OurClasses',
  data(){
    return{
        classesList : [
            {
                className : "Little Lambs",
                img : require("../../assets/images/class_01-690x506.jpg"),
                ageRange: "12-24",
                ageRangeName: "Months olds",
                classSize: "9",
            },
            {
                className : "Bouncy Bears",
                img : require("../../assets/images/class_02-690x506.jpg"),
                ageRange: "2-3",
                ageRangeName: "Years olds",
                classSize: "12",
            },
            
            {
                className : "Tenderhearts",
                img : require("../../assets/images/class_03-690x506.jpg"),
                ageRange: "3-4",
                ageRangeName: "Years Old",
                classSize: "15",
            },
            
            {
                className : "Shining Stars",
                img : require("../../assets/images/class_04-690x506.jpg"),
                ageRange: "4-5",
                ageRangeName: "Years Old",
                classSize: "20",
            },
            
            


        ]
    }
  }
 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#OurClasses{
    width: 100%;
    margin: 0 auto;
    // padding: 25px 0;
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
    .main-a {
        gap: 20px
    }
    .main-b{
        background-color: #f5f5f5;
        padding: 50px 15%;
        gap: 0;
        

        div.left {
            width: 50%;
            padding: 5px;
            // height: 200px;
            // border: 1px solid red;
            > * {
                margin: 25px 0;
            }
        }

    }
    .section-title > *{
        width: 50%;
    }
    .classContainer{
        width:100%;
        
        gap: 2%;
        justify-content: space-between;
        flex-wrap: wrap;
    }
    .classCard {
        //debug
        position: relative;
        width: 46%;
        margin: 1% 0;
        height: 150px;
        color: white;
        
        background-color: #56509f;
        .classCard-text {
            width:50%;
            padding: 15px;
            justify-content: space-between;
        }
        .classStats{


            div {
            gap: 5px;
            width: 50%;
            justify-content: center;
            align-items: center;
            }
            .classStats-1 {
                border-right: 1px solid white;
            }
        } 
        
        img {
            width:50%;
        }
        .minor {
            font-size: 0.8em;
        }
    }
    .cardContainer{
        width: 50%;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        gap: 5px
    }
    .card{
        width: 40%;
        min-height: 150px;
        
        justify-content: center;
        align-items: center;
        text-align: center;
        img{
        height: 35px;
        }
        h3 {
        margin: 10px 0;
        font-weight: bold;
        }
        p {
        font-size: 0.8rem;
        }
    }
    .absoluteBtn {
        position: absolute;
        right: 0;
        bottom: 0;
        z-index: 10;
        color: white;
        background-color: #fe6601;
        border:1px solid #fe6601;
        padding: 10px 15px;
        font-size: 0.8rem;
        font-weight: bold;

        &:hover {
            cursor: pointer;
            color: #fe6601;
            background-color: white;
        }
    
    }
    .round {
        width: 75px;
        height: 75px;
    }   
}


</style>