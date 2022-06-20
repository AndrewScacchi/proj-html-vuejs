<template>
  <div id="header" class="flex-row">
    <img id="logo" src="../assets/images/logo.png" alt="logoFable">
    <nav class="flex-row">
      <a href="" class="flex-col">
        <img src="../assets/img/home.png" alt="icn">
        <span>Home</span>
      </a>

      <a v-for="(navLink, i) in navLinks" :key="i" href="#" class="flex-col">
        <img :src="navLink.img" alt="icn">
        <span>{{navLink.text}}</span>
      </a>

    </nav>
  </div>
</template>

<script>
export default {
  name: 'MyHeader',


  data() {
    return {
      navLinks: [
        {
          text: "Home",
          img: require("../assets/img/home.png"),
          imgHover: require("../assets/img/home-2.png"),
        },
        {
          text: "Pages",
          img: require("../assets/img/document.png"),
          imgHover: require("../assets/img/document-2.png")
        }
      ]
    }
  }
}
 
    
//i need to create a database with all the nav link, text,img img2 and i need to create a function for hover functionality





</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  #header {
    width:100%;
    height: 100px;
    background: white;
    padding: 0 15%;
    justify-content: space-between;
    align-items: center;
  }
  #logo {
    height: 100%;
  }
nav{
  gap:10px;

  a{
    // display: inline-block;
    height: 100px;
    text-decoration: none;

    gap: 5px;
    
    justify-content: center;
    align-items: center;
    padding: 0 20px;
  
    // on hover nav link change color but we need to change icons too, create a dabatase i must
    &:hover{
      background-color: #fe6601;
      color: white;
    }

  }
}

</style>