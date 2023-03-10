<template>
    <div>
        <div class="container">
            <div class="row">
                <div class="col-12">
                     <h3  id="contact" class="p-5 text-center txt">Take a look at my <span style="color:orange">Work</span></h3>
    
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
            
            <div class="col-12">

                     <h2 class="pt-5 text-center txt">Gotta catch 'em <span style="color:orange">All</span></h2>
                     <p class="text-center">Click the picture below and search your own favourite Pokèmon</p>
                    <a href="https://pokedex-if.netlify.app/"><div><img src="../assets/img/pokemon.png" alt=""></div></a> 
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
.txt{
   
    font-size: 4rem;
    
}

img{
    width: 100%;
}
</style>