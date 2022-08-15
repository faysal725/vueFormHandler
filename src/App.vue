<template>
  <div>
    <app-header></app-header>
    <router-view></router-view>
  </div>
</template>

<script>


import addBlog from './Components/addBlog.vue'
import listBlogs from './Components/listBlogs.vue';
import showBlogs from './Components/showBlogs.vue';
import header from './Components/header.vue'

export default {
  components:{
    'add-blog': addBlog,
    'show-blogs':showBlogs,
    'list-blogs': listBlogs,
    'app-header': header
  },
  data(){

      return{
        
      }
  },
  methods: {
    
  }
}
</script>




<style>
  body{
    margin:0;
    font-family:'Nunito SemiBold';
  }
</style>