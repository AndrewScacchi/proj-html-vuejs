<template>
<!-- creating a Jumbotron with img and file in flex -->
  <div id="jumbo">
    <section class="mainJumbo">
      <div class="jumboText flex-col">
        <h2>Frendly Atmosphere</h2>
        <h1>
          <strong>Welcoming Place</strong> 
          for every child
        </h1>

        <button class="btn btn-orange">
          BUY THIS THEME NOW
        </button>
      </div>
        
    </section>
    <section class="blueBar flex-row">
      <h2>How to Enroll your child to a class?</h2>
      <button class="btn btn-blue">
        LEARN MORE >
      </button>

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

    section.mainJumbo {
        width: 100%;
        margin: 0 auto;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        gap: 25px;
        background: url("../../assets/images/slider_slide2_img1.png") 60% 50% no-repeat,
                    url("../../assets/images/slider_slide2_img2.png") 80% 50% no-repeat,
                    url("../../assets/images/slider_slide2_background.png") bottom repeat,
                    ;
        background-size: 300px, 250px, auto;
        height: 400px;
       


        .jumboText{
          align-self: center;
          justify-content: center;
          align-items: center;
          width: 30%;
          margin-left: 15%;
          margin-right: auto;
          height: 300px;
          gap:25px
          // border: 1px solid red;

        }
        .jumboImg{
          width: 60%;
        }
        
        
    }
    section.blueBar {
      background: #56509f;
      height: 100px;
      width: 100%;
      padding: 0 15%;
      align-items: center;
      justify-content: space-between;
      h2 {
        color: #fefffe;
        font-size: 2rem;
      }
      button{
        margin-right: 50px;
        
      }
    }

</style>