<template>
<!-- creating a Jumbotron with img and file in flex -->
  <div id="jumbo">
    <section class="mainJumbo">
      <div class="jumboText flex-col">
        <h3>Friendly Atmosphere</h3>
        <h1>Welcoming Place </h1>
        <h2>For Every Child</h2>

        <div class="btn btn-orange">
          BUY THIS THEME NOW
        </div>
      </div>
        
    </section>
    <section class="blueBar flex-row">
      <h2>How to Enroll your child to a class?</h2>
      <div class="btn btn-blue">
        LEARN MORE >
      </div>

    </section>
    
  </div>
</template>

<script>
export default {
  name: 'JumboTron',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

@import "../../assets/css/style.scss";

    section.mainJumbo {
        width: 100%;
        margin: 0 auto;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        gap: 10px;
        background: url("../../assets/images/slider_slide2_img1.png") 60% 50% no-repeat,
                    url("../../assets/images/slider_slide2_img2.png") 80% 50% no-repeat,
                    url("../../assets/images/slider_slide2_background.png") bottom repeat,
                    ;
        background-size: 300px, 250px, auto;
        height: 400px;
       


        .jumboText{       
          align-self: center;
          justify-content: center;
          text-align: left;
          width: 30%;
          margin-left: 15%;
          margin-right: auto;
          height: 300px;
          gap:5px;

          h1 {
            font-weight: bolder;
            font-size: 2.5em;
          }
          h2{
            font-size: 2em;
            font-weight: lighter;
          }
          h3{
            color: $blazeOrange;
            font-weight: lighter;
            font-size: 1.5em;
            // ahahah
            font-family: "Comic Sans MS", "Comic Sans", cursive;
          }
          div.btn{
            margin-top: 20px;
            max-width: 200px;
          }
          // border: 1px solid red;

        }
        .jumboImg{
          width: 60%;
        }
        
        
    }
    section.blueBar {
      background: $darkBlue;
      height: 100px;
      width: 100%;
      padding: 0 15%;
      align-items: center;
      justify-content: space-between;
      
      h2 {
        color: $sugarCane;
        font-size: 2rem;
        font-weight: lighter;
      }
      button{
        margin-right: 50px;
        
      }
    }

</style>