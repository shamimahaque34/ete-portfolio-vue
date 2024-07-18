<template>
<MyPageTitle/>
<MyService/>
<MyProjectIdea/>
</template>

<script>
import MyPageTitle from "@/components/services/MyPageTitle";
import MyProjectIdea from "@/components/services/MyProjectIdea";
import MyService from "@/components/services/MyService";
export default{
    name: 'ServiceView',
    components:{MyPageTitle,MyService,MyProjectIdea}
}
</script>

<style scoped>
</style>