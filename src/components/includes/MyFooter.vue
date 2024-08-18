<template>
  
  <footer>
        <div class="container">
          <div class="row footer">
            <div class="col-md-6 footer-content">
              <h3>About Me</h3>
              <p>
                I'm a Web Developer, based in Dhaka, Bangladesh. I did my bachelor
                in Computer Science and Engineering. I also underwent several
                trainings in Web Development at various renowned training
                institutions. I'm expert in HTML/HTML5, CSS/CSS3, Bootstrap 4, Tailwind CSS,
                Wordpress Theme Customization, Wordpress Theme Development, JavaScript, Php, Laravel, Vue Js and more.
              </p>
            </div>
  
            <div class="col-md-3 footer-content">
              <h3>Quick Links</h3>
              <div class="links">
                <ul>
                  <li><router-link to="/about">About Me</router-link></li>
                  <li><router-link to="/services">Services</router-link></li>
                  <li><router-link to="/portfolio">Portfolio</router-link></li>
                  <li><router-link to="/contact">Contact Me</router-link></li>
                </ul>
              </div>
            </div>
  
            <div class="col-md-3 footer-content">
              <h3>Get in Touch</h3>
              <div class="links" v-for="(contact,key) in contacts" :key="key">
                <ul>
                  <li><a href="#">{{ contact.phone }}</a></li>
                  <li><a href="#">{{ contact.email }}</a></li>
                  <li>
                    <a href="#">
                     {{ contact.address }}
                    </a>
                  </li>
                  <li>
                    <div class="footer-connect" >
                      <div class="tab-connect-info" >
                        <ul>
                          <li  v-for="(socialIcon,key) in socialIcons" :key="key">
                            <a
                              :href="socialIcon.link"
                              target="_blank"
                            >
                              <i v-bind:class="socialIcon.name"></i>
                            </a>
                          </li>
  
                         
                        </ul>
                      </div>
                    </div>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
        <div class="copy-right">
          <div class="container">
            <div class="row">
              <div class="col-md-12">
                <div class="text-center">
                  <p class="mb-0">
                    All Rights Reserved &copy; 2024 by
                    <router-link to="/about">Shamima Haque</router-link>
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </footer>
  </template>
  
  <script>
  import axios from "axios";
  export default{
    name: 'MyFooter',
    data(){

return{
   
   contacts :[],
   socialIcons : [],
}
},

created()
{
this.getContactInfo();
this.getSocialIconInfo();
},

methods:{
getContactInfo(){
    axios.get('https://admin.shamima.xyz/api/contact-info').then((response)=>{
        // console.log(response.data);
        this.contacts = response.data;
    });
},
getSocialIconInfo(){
    axios.get('https://admin.shamima.xyz/api/social-icon-info').then((response)=>{
        // console.log(response.data);
        this.socialIcons = response.data;
    });
}
   }
  }
  </script>
  <style scoped>
  </style>
  