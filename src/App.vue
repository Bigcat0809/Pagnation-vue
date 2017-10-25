<template>
  <div id="app">
    <img src="./assets/logo.png">
     <pagination :pageCount="pageCount" @togglePage="togglePage($event)"></pagination>
    <!-- <router-view/> -->
  </div>
</template>

<script>
import Pagination from './components/Pagination'
export default {
  name: 'app',
  components:{Pagination},
  data(){
    return{
      pageCount: 20
    }
  },
  methods:{
    togglePage(indexPage){
      //打印出当前页数
      console.log(indexPage);
    },
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
