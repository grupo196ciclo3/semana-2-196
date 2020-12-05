<template>
    
</template>

<script>

    import axios from "axios";

    export default {
        name:ComponenteApi,
        data(){
            return{
                movies: null
            }
        },
        mounted(){

            axios
            .get("URL")
            .then(response => (this.movies = response))
        }
    }
</script>

<style lang="stylus" scoped>

</style>