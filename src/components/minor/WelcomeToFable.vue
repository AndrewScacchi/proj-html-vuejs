<template>
<!-- creating a Jumbotron with img and file in flex -->
  <div id="WelcomeToFable" class="flex-col">


    <div class="title flex-col">
      <h1>Welcome to Fable</h1>
      <h5>Our contact adress and contact details</h5>
      <img src="../../assets/images/header_divider.png" alt="">

    </div>
    <section class="flex-row main-a">
       
        <div class="card">
            <div class="round round-orange">
                <img src="../../assets/images/globe_alt.png" alt="">
            </div>
            <h4>Morbi Etos</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum fuga rerum corrupti, odit aspernatur illum harum fugiat illo at laudantium asperiores nisi</p>
        </div>
        <div class="card">
            <div class="round round-blue">
                <img src="../../assets/images/stroller_alt.png" alt="">
            </div>
            <h4>Congue Gravidas</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum fuga rerum corrupti, odit aspernatur illum harum fugiat illo at laudantium asperiores nisi</p>
        </div>
        <div class="card">
            <div class="round round-orange">
                <img src="../../assets/images/bell_alt.png" alt="">
            </div>
            <h4>Maecenas Node</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum fuga rerum corrupti, odit aspernatur illum harum fugiat illo at laudantium asperiores nisi</p>
        </div>
        <div class="card">
            <div class="round round-blue">
                <img src="../../assets/images/globe_alt.png" alt="">
            </div>
            <h4>Praesent Morbi</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum fuga rerum corrupti, odit aspernatur illum harum fugiat illo at laudantium asperiores nisi</p>
        </div>
    
    </section>
    <section class="flex-row main-b">
    
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
  min-height: 200px;
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
    .card{
    
    width: 15%;
    justify-content: center;
    align-items: center;
    text-align: center;
    img{
      height: 60px;
    }
    h4 {
      margin: 10px 0;
      font-weight: bold;
    }
    p {
      font-size: 0.8rem;
    }
  }
  }
  .main-b{
    background-color: grey;
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
  
}

</style>