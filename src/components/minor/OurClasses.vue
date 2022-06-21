l<template>
<!-- creating a Jumbotron with img and file in flex -->
  <div id="ourClasses" class="flex-col">


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
            <!-- <div v-for="(classe, i) in classesList" :key="i" class="classCard flex-row">
                
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
                
                <img class="classCard-img" :src="classe.img" :alt="classe.className">
               
                <div class="absoluteBtn">
                    READ MORE >
                </div>

            </div>  -->
            
            <!-- props -->
            <classCard v-for="(singleClass, i) in classesList" :key="i" 
                :nombre="singleClass.className"
                :imagen="singleClass.img"
                :edad="singleClass.ageRange"
                :edadTipo="singleClass.ageRangeName"
                :numero="singleClass.classSize"
            />
        </div>
    </section>
    <section class="main-b flex-row">
        <div class="left">
            <h2>We have been educating children for over fifteen years. Our goal is to create a place that engages each child.</h2>
            <p> Molestias consequatur iure culpa voluptatem voluptatum id dignissimos ea maiores, magnam, cum quas excepturi aliquam inventore dolore in quis necessitatibus facilis ratione?</p>
            <!-- yes the list is static. Is just a list! -->
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
        <!-- This are static -->
        <div class="cardContainer flex-row">
            <div class="card flex-col">
                <div class="round round-white">
                    <img src="../../assets/images/toy.png" alt="">
                </div>
                <h3>Learning&Fun</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. </p>
            </div>
            <div class="card flex-col">
                <div class="round round-white">
                    <img src="../../assets/images/meal.png" alt="">
                </div>
                <h3>Healthy Meals</h3>
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
                    <img src="../../assets/images/shield.png" alt="">
                </div>
                <h3>Children Safety</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. </p>
            </div>

        </div>
        

    </section>
    
    
    
    
  </div>
</template>

<script>
import classCard from './classCard.vue'
export default {
    name: "OurClasses",
    data() {
        return {
            classesList: [
                {
                    className: "Little Lambs",
                    img: require("../../assets/images/class_01-690x506.jpg"),
                    ageRange: "12-24",
                    ageRangeName: "Months olds",
                    classSize: "9",
                },
                {
                    className: "Bouncy Bears",
                    img: require("../../assets/images/class_02-690x506.jpg"),
                    ageRange: "2-3",
                    ageRangeName: "Years olds",
                    classSize: "12",
                },
                {
                    className: "Tenderhearts",
                    img: require("../../assets/images/class_03-690x506.jpg"),
                    ageRange: "3-4",
                    ageRangeName: "Years Old",
                    classSize: "15",
                },
                {
                    className: "Shining Stars",
                    img: require("../../assets/images/class_04-690x506.jpg"),
                    ageRange: "4-5",
                    ageRangeName: "Years Old",
                    classSize: "20",
                },
            ]
        };
    },
    components: { classCard }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/css/style.scss";

#ourClasses{
    @include main-id-style;



    section{
        justify-content: center;
        align-items: center;
        width: 100%;
        padding: 25px 15%;
        gap: 5%;
        
    }
    .main-a {
        gap: 20px;
    }
    .main-b{
        background-color: $darkWhite;
        padding: 50px 15%;
        gap: 0;
        div.left {
            width: 50%;
            padding: 5px;
            
            > * {
                margin: 25px 0;
            }
        }

    }
    .section-title{
        gap: 1%;
        justify-content: space-between;
        & > *{
        width: 49%;
    }
    }
    .classContainer{
        width:100%;
        
        gap: 1%;
        justify-content: space-between;
        flex-wrap: wrap;
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
   
    .round {
        width: 75px;
        height: 75px;
    }   
}
ul {
  list-style-image: url('../../assets/images/style_1.png');
  list-style-position: inside;
  li{
    line-height: 1.8em;
    font-size: 1em;
  }
}

</style>