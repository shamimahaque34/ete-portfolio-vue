<template>
   
<div class="container section-padding banner">
    <div class="row">
        <div class="col-12 col-sm-12 col-md-6 col-lg-6 col-xl-6 banner-content">
           
           <h3>Looking for...</h3>


           
          <h1>
                <span class="type" id="typedMessage"></span>
            </h1>
            
           
                <p>Let me provide <span>High-Quality</span> web developement services  <br>
                   at an <span>Affordable</span> cost.
                </p>
                
            <router-link to="/about"><button type="button" @click="active = 'about'" class="main-button" :class="{active:active === 'about'}">About</button></router-link>
            <router-link to="/portfolio">
            <button type="button"  @click="active = 'portfolio'" class="another-button" :class="{active:active === 'portfolio'}"> Recent Projects</button></router-link>
  
        </div>
        <div class="col-12 col-sm-12 col-md-6 col-lg-6 col-xl-6 banner-img">
            <img src="/assets/images/banner-img.svg" alt="img">
        </div>
    </div>
</div>

</template>


<script>

import Typed from 'typed.js';

 export default{
    name:'MyBanner',
    data(){
        return{
            active: null ,
            typed : '',
            
        };
    },

    mounted(){
        this.typed = new Typed('#typedMessage',{
                strings:["Web Design?",
                "Web Development?",
                "A WordPress Website?",
                "eCommerce Solution?",],
                typeSpeed:50,
                backSpeed: 60,
                loop: true
        });
    }

    
}

</script>


<style scoped></style>