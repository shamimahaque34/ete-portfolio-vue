<template>
    <MyPortfolio/>
    <MyTestimonial/>
</template>
    
    <script>
     import MyPortfolio from "@/components/portfolio/MyPortfolio";
     import MyTestimonial from "@/components/portfolio/MyTestimonial";
    export default{
        name: 'PortfolioView',
        components:{MyPortfolio,MyTestimonial}
    }
    </script>
    
    <style scoped>
    </style>