<template>
<div class="container section-padding">
    <div class="row">
        <div class="col-12 col-sm-12 col-md-12 col-lg-12 col-xl-12">
          <carousel>
            <div id="testimonial-slider" class="">
                <div class="testimonial">
                    <div class="client">
                        <img src="/assets/images/profile.jpeg" alt="">
                    </div>
                    <div class="testimonial-content">
                        <p class="description">
                            I'm a Web Developer, based in Dhaka, Bangladesh. I did my bachelor
                          in Computer Science and Engineering. I also underwent several
                          trainings in Web Development at various renowned training
                          institutions. I'm expert in HTML/HTML5, CSS/CSS3, Bootstrap 4, Tailwind CSS,
                          Wordpress Theme Customization, Wordpress Theme Development,JavaScript, Php, Laravel, Vue Js and more.
                        </p>
                        <h3 class="client-title">Shamima
                            <small class="post">Web Developer</small>
                        </h3>
                    </div>
                </div>
 
               
                
            </div>
        </carousel>
       
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
    axios.get('http://localhost/ete-portfolio/public/api/testimonial-info').then((response)=>{
        console.log(response.data);
        // this.infos = response.data;
    });
}
}

}
</script>

<style scoped>
</style>