<template>
    <nav class="navbar navbar-expand-lg sticky-top navbar-dark bg-success ">
        <a class="navbar-brand " href="# ">
        <img :src="require('./')" width="50 " height="50
        " class="d-inline-block align-center mr-2" alt="Logo" loading="lazy"><span class="font-weight-bold">LANGUAGE
            MASTER</span>
        </a>
        <button class="navbar-toggler d-lg-none" type="button" data-toggle="collapse"
        data-target="#collapsibleNavId" aria-controls="collapsibleNavId" aria-expanded="false"
        aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse justify-content-end " id="collapsibleNavId">
            <ul class="navbar-nav ">
                <li class="nav-item active ">
                    <a class="nav-link h5 font-weight-bold " href="#">Home<span class="sr-only ">(current)</span></a>
                </li>
                <li class="nav-item active">
                    <a class="nav-link h5 font-weight-bold" href="#services">Services</a>
                </li>
                <li class="nav-item active">
                    <a class="nav-link h5 font-weight-bold" href="#movies">Movies</a>
                </li>
                <li class="nav-item active">
                    <a class="nav-link h5 font-weight-bold" href="#news">News</a>
                </li>
                <li class="nav-item active">
                    <a class="nav-link h5 font-weight-bold " href="#team">Team</a>
                </li>
            </ul>
        </div>
    </nav>
</template>

<script>
    export default {
        name: "ComponenteNav",
        data(){
            return{
                imagen: "../"
            }
        }
    }
</script>

<style lang="stylus" scoped>

</style>