<template>
    <div>
        <nuxt-child :video="video"/>
    </div>
</template>

<script>
import {mapState} from 'vuex'
    export default {

      
        //    async asyncData(context) {
        //     let response = await context.$axios.get('https://jsonplaceholder.typicode.com/posts')
        //     let videos = response.data
           
        //     return{
        //         videos
                
        //     }
            
        // },
         async fetch({$axios, store}) {
            let response = await $axios.get('https://jsonplaceholder.typicode.com/posts')
            let video = response.data
           
           store.commit('SET_CURRENT_VIDEO', video)
            
        },
     
        computed:{
            ...mapState({
                video: 'currentVideo'
            })

        }
    }
</script>

<style lang="scss" scoped>

</style>