<template>
    <div class="container services-section-padding">
        <div class="row">

            <div class="col-md-4"  v-for="(service,key) in services" :key="key">
                <div class="single-service">
                    <div class="service-icon">
                        <i v-bind:class="service.service_icon"></i>
                     
                    </div>
                    <h4>{{ service.title }}</h4>
                    <p>{{ service.description }}</p>
                    <div class="service-hover"></div>
                </div>
            </div>
            
           
        </div>
       
    </div>
  </template>
  
  
  <script>
//   import Vue from 'vue'
// import { library } from '@fortawesome/fontawesome-svg-core'
// import { faUserSecret } from '@fortawesome/free-solid-svg-icons'
// import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

// library.add(faUserSecret)
// Vue.component('font-awesome-icon', FontAwesomeIcon)
// Vue.config.productionTip = false;
import axios from "axios";

  export default{
    name:'MyService',
    data(){

return{
    
   services :[],
   icons: ["laravel", "wordpress-simple"],
}
},

created()
{
this.getServiceInfo();
},

methods:{
getServiceInfo(){
    axios.get('http://localhost/ete-portfolio/public/api/service-info').then((response)=>{
        // console.log(response.data);
        this.services = response.data;
    });
}
}
}
    
  
  </script>
  
  
  <style scoped>
  
  </style>
  