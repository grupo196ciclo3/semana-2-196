<template>
    <div>
        <componente-nav></componente-nav>
        <div id="carouselExampleCaptions" class="carousel slide" data-ride="carousel">
            <ol class="carousel-indicators">
                <li data-target="#carouselExampleCaptions" data-slide-to="0" class="active"></li>
                <li data-target="#carouselExampleCaptions" data-slide-to="1" class=""></li>
                <li data-target="#carouselExampleCaptions" data-slide-to="2" class=""></li>
            </ol>
            <div class="carousel-inner">
                <div class="carousel-item active">
                <img src="https://academiagoma.com/wp-content/uploads/2018/10/10-razones-para-aprender-ingles-academia-goma-talavera-de-la-reina.jpg" alt="Banner1" class="img-fluid" width="100%">
                </div>
                <div class="carousel-item">
                <img src="https://assets.entrepreneur.com/content/3x2/2000/1598024927-ingles1.jpg?width=700&crop=2:1" alt="Banner1" class="img-fluid" width="100%">
            </div>
            <div class="carousel-item">
                <img src="https://www.lincolnenglishcenter.com/images/blog/research-papers-english-language-and-fair-play2.png" alt="Banner1" class="img-fluid" width="100%">
                <div class="carousel-caption d-none d-md-block">
                    <h3 class="p-3 bg-light rounded text-danger font-weight-bold font-italic">"Vives una nueva vida por
                    cada
                    idioma nuevo que hablas. Si conoces sólo un idioma, sólo vives una vez" -Proverbio checo</h3>
                </div>
            </div>
            </div>
            <a class="carousel-control-prev" href="#carouselExampleCaptions" role="button" data-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="sr-only">Previous</span>
            </a>
            <a class="carousel-control-next" href="#carouselExampleCaptions" role="button" data-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                <span class="sr-only">Next</span>
            </a>
        </div>
    </div>
</template>

<script>
import ComponenteNav from "./ComponenteNav.vue"
    export default {
        name: "ComponenteBanner",
        components: {
            ComponenteNav
        }
    }
</script>

<style lang="stylus" scoped>

</style>