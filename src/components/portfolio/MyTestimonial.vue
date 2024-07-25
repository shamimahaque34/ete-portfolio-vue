<template>
     <div class="container section-padding">
    <div class="row">
        <div class="col-md-12">
            <div id="testimonial-slider" class="">
                <div class="testimonial" v-for="(info,key) in infos" :key="key">
                    <div class="client">
                        <img :src="info.image" alt="">
                    </div>
                    <div class="testimonial-content">
                        <p class="description">
                           {{ info.description }}
                        </p>
                        <h3 class="client-title">{{ info.name }}
                            <small class="post">{{ info.designation }}</small>
                        </h3>
                    </div>
                </div>
 
               
            </div>
        </div>
    </div>
</div>     
  </template>
  
  
  <script>
  import axios from "axios";
  export default{
    name:'MyTestimonial',
    data(){

return{
   
   infos :[],
}
},

created()
{
this.getTestimonialInfo();
},

methods:{
getTestimonialInfo(){
    axios.get('http://localhost/ete-portfolio/public/api/testimonial-info').then((response)=>{
        // console.log(response.data);
        this.infos = response.data;
    });
}
}

  }
  </script>
  
  
  <style scoped>
  
  </style>
  