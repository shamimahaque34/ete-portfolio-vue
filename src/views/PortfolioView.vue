<template>
    <MyPageTitle/>
    <MyPortfolio/>
    <MyTestimonial/>
</template>
    
    <script>
    import MyPageTitle from "@/components/portfolio/MyPageTitle";
     import MyPortfolio from "@/components/portfolio/MyPortfolio";
     import MyTestimonial from "@/components/portfolio/MyTestimonial";
    export default{
        name: 'PortfolioView',
        components:{MyPageTitle,MyPortfolio,MyTestimonial}
    }
    </script>
    
    <style scoped>
    </style>