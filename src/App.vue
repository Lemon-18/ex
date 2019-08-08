<template>
  <div id="app">
      <Top/>
      <Nav v-if="$route.meta.tabBar"></Nav>
      <router-view></router-view>
      
     
  </div>
</template>
<script>
import Top from "common/top";
import Nav from "common/tableBar"
export default{
  name:"App",
  components:{
    Nav,
    Top
  }
}
</script>
<style lang="scss">
#app{
  font-size:.12rem;
  
}
</style>
