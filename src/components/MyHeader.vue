<template>
  <div id="header" class="flex-row">
    <img id="logo" src="../assets/images/logo.png" alt="logoFable">
    <nav class="flex-row">

      <!-- dynamic navLink from data -->
      <!-- the @mouse are used to change to hover tracker-->
      <a v-for="(navLink, i) in navLinks" :key="i" :href="navLink.idTag" class="flex-col"
        @mouseover="navLink.hover = true"
        @mouseleave="navLink.hover = false"
        >
        <!-- if hover -->
        <img v-if="navLink.hover" :src="navLink.imgHover" :alt="navLink.text">
        <!-- if else -->
        <img v-else :src="navLink.img" :alt="navLink.text">
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
          hover: false,
          idTag : "#",
        },
        {
          text: "Pages",
          img: require("../assets/img/document.png"),
          imgHover: require("../assets/img/document-2.png"),
          hover: false,
          idTag : "#welcomeToFable",
        },
        {
          text: "Blog",
          img: require("../assets/img/printer.png"),
          imgHover: require("../assets/img/printer-2.png"),
          hover: false,
          idTag : "#whatIsNew",
        },
        {
          text: "Shop",
          img: require("../assets/img/cart.png"),
          imgHover: require("../assets/img/cart-2.png"),
          hover: false,
          idTag : "#",
        },
        {
          text: "Shortcodes",
          img: require("../assets/img/lab.png"),
          imgHover: require("../assets/img/lab-2.png"),
          hover: false,
          idTag : "#ourClasses",
        },
        {
          text: "Support",
          img: require("../assets/img/chat.png"),
          imgHover: require("../assets/img/chat-2.png"),
          hover: false,
          idTag : "#",
        },
        {
          text: "Contact",
          img: require("../assets/img/envelope.png"),
          imgHover: require("../assets/img/envelope-2.png"),
          hover: false,
          idTag : "#contactUs",
        }
      ]
    }
  }
}
 
    
//i need to create a database with all the nav link, text,img img2 and i need to create a function for hover functionality





</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/css/style.scss";
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
  background-color: $white;
  a{
    height: 100px;
    text-decoration: none;
    color: #444275;

    gap: 5px;
    
    justify-content: center;
    align-items: center;
    padding: 0 20px;
    img{
      height: 25px;
    }
    // on hover nav link change color but we need to swap icons too
    &:hover{
      background-color: $blazeOrange;
      color: $sugarCane;
    }

  }
}

</style>