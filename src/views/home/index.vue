<template>
    <div id = "home">
        <Classify/>
        <Albums/>
        <!-- <router-view></router-view> -->
    </div>
    </template>
    
    <script>
    import Classify from "components/classify";
    import Albums from "components/albumList"
    export default{
        name:"recoContent",
        components:{
            Classify,
            Albums
        }
    }

</script>
<style>

</style>