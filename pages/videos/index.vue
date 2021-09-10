<template>
    <div class="videocontainer">
    <h1>Videos</h1>
    <div  v-for="video in $store.state.videos"
    :key="video.id"
   >
    <nuxt-link class="links" :to="`/videos/${video.id}`"> -> {{video.title}}</nuxt-link></div>
    
    </div>
  
</template>

<script>
    export default {
        head:{
            title:'Learn Nuxt Js - Videos'
        },
        // async asyncData(context) { axiosiçin vuex değil
        //     let response = await context.$axios.get('https://jsonplaceholder.typicode.com/posts')
        //     let videos = response.data
           
        //     return{
        //         videos
                
        //     }
            
        // }, 

           async fetch({$axios, store}) {
            let response = await $axios.get('https://jsonplaceholder.typicode.com/posts')
            let videos = response.data
           
            store.commit('SET_VIDEOS', videos);
            
        },
    }
</script>

<style  scoped>
.videocontainer{
    width: 80%;
    margin: 0 auto;
}
h1{
color: tomato;
}
.links{
    text-decoration: none;
    color: rgb(61, 59, 59);

}
</style>