<template>
<!-- creating a Jumbotron with img and file in flex -->
  <div id="contactUs" class="flex-col">


    <div class="contact-title flex-col">
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
    <form action="get" class="contact-form flex-row">
      <div class="form-data flex-col">
        <input type="text" placeholder="Your Name *" required>
        <input type="mail" placeholder="Your E-mail *" required>
        <input type="text" placeholder="Subject">
      </div>
      <textarea class="form-msg" placeholder="Your Message *" required></textarea>

      <input id="form-btn" type="button" value="SEND MESSAGE" class="btn btn-orange">
    </form> 
    
    
  </div>
</template>

<script>
export default {
  name: 'WelcomeToFable',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#contactUs{
  width: 70%;
  margin: 0 auto;
  min-height: 200px;
  padding: 25px 0 75px;
  align-items: center;
  justify-content: space-around;
  gap: 25px;
  .contact-title{
    justify-content: center;
    align-items: center;
    img{
        margin: 20px auto;
    }
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
  
}

</style>