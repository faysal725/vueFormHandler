<template>
  <div>
    <show-blogs></show-blogs>
  </div>
</template>

<script>


import addBlog from './Components/addBlog.vue'
import showBlogs from './Components/showBlogs.vue';

export default {
  components:{
    'add-blog': addBlog,
    'show-blogs':showBlogs
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