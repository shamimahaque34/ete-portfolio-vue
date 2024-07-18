<template>
    <MyPageTitle/>
    <MyContact/>
  
    </template>
    
    <script>
    import MyPageTitle from "@/components/contact/MyPageTitle";
    import MyContact from "@/components/contact/MyContact";
    
    export default{
        name: 'ContactView',
        components:{MyPageTitle,MyContact}
    }
    </script>
    
    <style scoped>
    </style>