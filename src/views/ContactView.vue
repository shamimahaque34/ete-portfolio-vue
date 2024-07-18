<template>
    <MyPageTitle/>
    <MyContact/>
    <MyMap/>
  
    </template>
    
    <script>
    import MyPageTitle from "@/components/contact/MyPageTitle";
    import MyContact from "@/components/contact/MyContact";
    import MyMap from "@/components/contact/MyMap";
    
    
    export default{
        name: 'ContactView',
        components:{MyPageTitle,MyContact,MyMap}
    }
    </script>
    
    <style scoped>
    </style>