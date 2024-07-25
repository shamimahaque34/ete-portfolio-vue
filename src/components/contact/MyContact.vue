<template>
   <div class="container">
      <div class="row">
        <div class="col-md-6 details-left connect-info" v-for="(contact,key) in contacts" :key="key">
          <div class="info-item">
            <strong>Phone</strong>
            <p class="mb-0">{{ contact.phone }}</p>
          </div>

          <div class="info-item">
            <strong>Email</strong>
            <p class="mb-0">{{ contact.email }}</p>
          </div>

          <div class="info-item">
            <strong>Address</strong>
            <p class="mb-0">{{ contact.address }}</p>
          </div>
        </div>

        <div class="col-md-6">
          <form class="contact-form">
            <input type="text" name="name" placeholder="Your name" />
            <input type="text" name="email" placeholder="Your email" />
            <textarea
              name="message"
              rows="4"
              placeholder="Your message"
            ></textarea>

            <button type="submit" name="send" class="main-button">
              Send Message
            </button>
          </form>
        </div>
      </div>
    </div>
  </template>
  
  
  <script>
  import axios from "axios";
  export default{
    name:'MyContact',
    data(){

return{
   
   contacts :[],
}
},

created()
{
this.getContactInfo();
},

methods:{
getContactInfo(){
    axios.get('http://localhost/ete-portfolio/public/api/contact-info').then((response)=>{
        // console.log(response.data);
        this.contacts = response.data;
    });
}
  }
}
  </script>
  
  
  <style scoped>
  
  </style>
  