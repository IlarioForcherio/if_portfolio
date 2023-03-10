<template>
    <div>
        <h2>this is Works</h2>
        <div class="container">
            <div class="row">
                <div class="col">
    
    <!-- slider-video -->
                    <div id="carouselExampleFade" class="carousel slide carousel-fade">
                        <div class="carousel-inner">
                            <div class="carousel-item active">
    
                                <iframe width="100%" height="500" src="https://www.youtube.com/embed/8PRl3J8KlKQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
                            </div>
                            <div class="carousel-item">
                                <iframe width="100%" height="500" src="https://www.youtube.com/embed/DiLwQ73z-gQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
                            </div>
                            <div class="carousel-item">
                                <iframe width="100%" height="500" src="https://www.youtube.com/embed/DiLwQ73z-gQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
                            </div>
                            <div class="carousel-item">
                                <iframe width="100%" height="500" src="https://www.youtube.com/embed/L3eyiwgfdGE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
                            </div>
                        </div>
                        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleFade" data-bs-slide="prev">
                              <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                              <span class="visually-hidden">Previous</span>
                        </button>
                        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleFade" data-bs-slide="next">
                              <span class="carousel-control-next-icon" aria-hidden="true"></span>
                              <span class="visually-hidden">Next</span>
                        </button>
                    </div>
                </div>
            </div>
        </div>
    
    </div>
</template>

<script>
// Importa qui i componenti necessari

export default {
    name: 'WorksView', // Cambia il nome del componente con quello desiderato
    components: {
        // Aggiungi qui i componenti importati
    },
    props: {

    },
    data() {
        return {
            // Inserisci qui i dati del tuo componente
        };
    },

    mounted() {
        // Inserisci qui il codice da eseguire quando il componente viene montato
    },
    methods: {

    },
};
</script>

<style lang="scss" scoped>
/* Inserisci qui il codice SCSS per lo stile del tuo componente */
</style>