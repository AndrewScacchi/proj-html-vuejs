<template>
<!-- creating a Jumbotron with img and file in flex -->
  <div id="contactUs" class="flex-col">


    <div class="title flex-col">
      <h1>Contact Us</h1>
      <h5>Our contact adress and contact details</h5>
      <img src="../../assets/images/header_divider.png" alt="">

    </div>
    <div class="contact-links flex-row">
     
      <!-- dynamic contact card -->
     
      <div v-for="(contactLink, i ) in contactLinks " :key="i" class="contact-card flex-col">
        <img :src="contactLink.img" :alt="contactLink.title">
        <h4>{{contactLink.title}}</h4>
        <p>{{contactLink.line1}}</p>
        <p>{{contactLink.line2}}</p>
        <p>{{contactLink.line3}}</p>
        <a href="">{{contactLink.contentLink}}</a>

      </div>


    </div>
    <form id="myForm" action="get" class="contact-form flex-row">
      <div class="form-data flex-col">
        <input type="text" placeholder="Your Name *" name="userName" required>
        <input type="mail" placeholder="Your E-mail *" name="userMail" required>
        <input type="text" placeholder="Subject" >
      </div>
      <textarea class="form-msg" placeholder="Your Message *" required name="userMsg"></textarea>

      <input @click="send" id="form-btn" type="button" value="SEND MESSAGE" class="btn btn-orange">
    </form> 
    
    
  </div>
</template>

<script>
export default {
  name: 'WelcomeToFable',
  methods: {
    send(){
      let a = document.forms["myForm"]["userName"].value;
      let b = document.forms["myForm"]["userMail"].value;
      let c = document.forms["myForm"]["userMsg"].value;
      if (a == "" || b == "" || c == "") {
        alert("One or more required field are missing");
        return false;
      }
      document.getElementById("myForm").reset();
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/css/style.scss";
#contactUs{
  @include main-id-style;
  padding: 25px 15%;
  }
.contact-links{
  justify-content: center;
  align-items: center;
  width: 100%;
  gap: 5%;
  .contact-card{
    width: 15%;
    justify-content: center;
    align-items: center;
    text-align: center;
    img{
      height: 30px;
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
.contact-form{
  margin-bottom: 100px;
  width: 100%;
  height: 100px;
  gap: 2%;
  flex-wrap: wrap;
  div {
    width: 49%;
    justify-content: space-between;
    gap: 10px;
    input {
      width: 100%;
      line-height: 25px;
      padding: 0 5px;
    }
  } 
  .form-msg{
    width: 49%;
    padding: 5px;
    resize: none;
  }
  #form-btn {
    padding: 5px;
    margin: 25px auto;
  }
}
  


</style>