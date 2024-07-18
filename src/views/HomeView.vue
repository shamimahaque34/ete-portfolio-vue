<template>
  <div class="home">
    <MyBanner/>
    <MyProjectIdea/>
    <MyTestimonial/>
    
  </div>
</template>



<script>
import MyBanner from "@/components/home/MyBanner";
import MyProjectIdea from "@/components/home/MyProjectIdea";
import MyTestimonial from "@/components/home/MyTestimonial";
export default {
  name: 'HomeView',
  components : {MyBanner,MyProjectIdea,MyTestimonial}
}
</script>

<style scoped>
</style>
