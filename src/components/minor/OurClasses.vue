l<template>
<!-- creating a Jumbotron with img and file in flex -->
  <div id="WelcomeToFable" class="flex-col">


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
    <section class="main-b">
        

    </section>
    
    
    
    
  </div>
</template>

<script>
export default {
  name: 'WelcomeToFable',
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
#WelcomeToFable{
    width: 100%;
    margin: 0 auto;
    padding: 25px 0 75px;
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
        padding: 25px;
        background-color: #f5f5f5;
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
}

</style>