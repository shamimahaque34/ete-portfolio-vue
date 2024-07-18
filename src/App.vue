<template>
  <MyNavbar/>
  <router-view/>
  <MyFooter/>
</template>

<script>
import  MyNavbar from "@/components/includes/MyNavbar";
import  MyFooter from "@/components/includes/MyFooter";
   export default{
    name: 'App',
    components :{MyNavbar,MyFooter}
   }
</script>
<style scoped>
</style>
