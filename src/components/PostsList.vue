<template>
    <div>
        <!-- <button @click="getPosts">Load Posts</button> -->
        <h3 v-if="errMsg">{{errMsg}}</h3>
        <div v-for="post in posts" :key="post.id">
            <h3>{{post.id}}. {{post.title}}</h3>
            <p>{{post.body}}</p>
            <hr />
        </div>
    </div>
</template>

<script>
import axios from 'axios'

    export default {
        name:"PostsList",
        created(){
            this.getPosts();
        },
        data(){
            return{
                posts : [],
                errMsg : ""
            }
        },
        methods:{
            getPosts(){
                axios.get('http://jsonplaceholder.typicode.com/posts')
                    .then((response)=>{
                        console.log(response.data)
                        this.posts = response.data
                    })
                    .catch((error)=>{
                        console.log(error);
                        this.errMsg = "Something went wrong"
                    })
            }
        }
    }
</script>

<style scoped>

</style>