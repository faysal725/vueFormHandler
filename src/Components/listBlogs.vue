<template>
    <div v-theme:column="'wide'" id="show-blogs">
        <h1>list blog titles</h1>
        <input type="text" v-model="search" placeholder="search blogs" />
        <div v-for="blog in filterBlogs" class="single-blog">
            <h2 v-rainbow>{{blog.title | to-uppercase}}</h2>
        </div>
    </div>
</template>

<script>
import searchMixin from '../mixins/searchMixin';
export default {
    
    data() {
        return {
            blogs:[],
            search:""
        };
    },
    methods: {
        
    },
    created(){
        this.$http.get('https://jsonplaceholder.typicode.com/posts').then(function(data){
            this.blogs = data.body.slice(0,10)

        })
    },
    computed:{

        
    },
    filters:{
        toUppercase(value) {

            return value.toUpperCase()
        }
    },
    directives:{
        'rainbow': {
            bind(el, binding, vnode){
                
                el.style.color = "#" + Math.random().toString().slice(2, 8)
                
            }
        }
    },
    mixins:[searchMixin]
};
</script>

<style scoped>
#show-blogs{
    max-width: 800px;
    margin:0 auto;
}

#show-blogs input {
    width:100%;
}
.single-blog{
    padding: 20px;
    margin: 20px 0;
    box-sizing: border-box;
    background: #eee;
}
</style>



