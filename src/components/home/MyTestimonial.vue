<template>
<div class="container section-padding">
    <div class="row">
        <div class="col-12 col-sm-12 col-md-12 col-lg-12 col-xl-12">
    
            <div id="testimonial-slider" class="">
                <div class="testimonial" v-for="(info,key) in infos" :key="key">
                    <div class="client">
                        <img v-bind:src="info.image" alt="">
                    </div>
                    <div class="testimonial-content">
                        <p class="description" v-html="info.description">
                          
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

// import carousel from "vue-owl-carousel";

export default{
    name: 'MyTestimonial',
    // components: { carousel },
  
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
    axios.get('https://admin.shamima.xyz/api/testimonial-info').then((response)=>{
        // console.log(response.data);
        this.infos = response.data;
    });
}
}

}
</script>

<style scoped>
</style>