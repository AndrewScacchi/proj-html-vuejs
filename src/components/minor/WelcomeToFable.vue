<template>
<!-- creating a Jumbotron with img and file in flex -->
  <div id="WelcomeToFable" class="flex-col">


    <div class="title flex-col">
      <h1>Welcome to Fable</h1>
      <h4>Our contact adress and contact details</h4>
      <img src="../../assets/images/header_divider.png" alt="">

    </div>
    <section class="flex-row main-a">
       
        <div class="card">
            <div class="round round-orange">
                <img src="../../assets/images/globe_alt.png" alt="">
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
                <img src="../../assets/images/bell_alt.png" alt="">
            </div>
            <h3>Maecenas Node</h3>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum fuga rerum corrupti,laudantium asperiores nisi</p>
        </div>
        <div class="card">
            <div class="round round-blue">
                <img src="../../assets/images/globe_alt.png" alt="">
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
                    <div class="btn btn-orange" >Our Mission</div>
                </div>
                <h2 class="left-title">Our philosphy is learning through play as we offer a stimulating enviroment for children. </h2>
                <div class="smallCard flex-row">
                    <div class="smallCard-img">
                        <img src="../../assets/images/clock_alt.png" alt="">
                    </div>
                    <div class="smallCard-text">                       
                        <h3>placeholder</h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Doloremque tempore dicta blanditiis pariatur, amet.</p>
                    </div>

                </div>
                <div class="smallCard flex-row">
                    <div class="smallCard-img">
                        <img src="../../assets/images/clock_alt.png" alt="">
                    </div>
                    <div class="smallCard-text">                       
                        <h3>placeholder</h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Doloremque tempore dicta blanditiis pariatur, amet.</p>
                    </div>

                </div>
                

            </div>
            <!-- right div -->
            <div class="section-right">

            </div>
            
        </div>

    </section>
    
    
    
    
  </div>
</template>

<script>
export default {
  name: 'WelcomeToFable',
 
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
    .section-container {
        width: 100%;
        padding: 0 15%;
        
        .section-left, .section-right{
            
            width: 50%;
            //debug
            border: 1px solid blue;
        }
        .section-left {
            padding: 20px ;
        }
        
    }

    
    //debug
    min-height: 200px;
    background-color: white;
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
    background-color: #f5f5f5;
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
        background: #fe6601;
        width: 75px;
        height: 75px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
    
    }
}

</style>