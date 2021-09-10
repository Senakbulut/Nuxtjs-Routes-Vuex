<template>
    <div>
        <h1>Editing {{$route.params.id}} - {{video.title}}</h1>
        <nuxt-link :to="`/videos/${video.id}`">
        <button>Go back</button>
        </nuxt-link>
    </div>
</template>

<script>
    export default {
       props:['video'] 
    }
</script>

<style lang="scss" scoped>

</style>