<template>
<!-- creating a Jumbotron with img and file in flex -->
  <div id="jumbo">
    <section>
        <div class="jumboText">
          <h2>minorPlaceholder</h2>
          <h1>placeholder</h1>
          
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

    section {
        width: 80%;
        margin: 0 auto;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        gap: 25px;
        .jumboText{
          width: 30%;

        }
        .jumboImg{
          width: 60%;
        }
    }


</style>