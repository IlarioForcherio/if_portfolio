<template>
    <div>
    
        <div class="container-fluid">
            <!-- intestazione -->
            <div class="row vh70 align-items-center">
                <div class=" col-sm-12 col-lg-6">
                    <h1 class="txt">Hi, nice to meet you, my name is</h1>
                </div>
                <div class="col-sm-12 col-lg-6">
                    <div class="">
                        <h2 class=" text-center"><span style='color:orange'>Ilario</span>  Forcherio</h2>
                        <h3 class=" text-center">Web <span style='color:orange'>Developer</span></h3>
                    </div>
                    <!-- <p class="text-center">"Mi chiamo Ilario e sono un Junior Full Stack Developer. Prima di approdare nel mondo dello sviluppo web ho lavorato molti anni in un settore diverso, fino al momento in cui ho deciso che avrei voluto cambiare vita per accoglierenuove
                        sfide. Il Master Boolean me ne ha dato la possibilita' e ha trasformato in poco tempo una nuova scoperta in una grande passione. Ho imparato a mettermi in gioco e voglio continuare a farlo, quotidianamente e con entusiasmo."</p> -->
                </div>
            </div>
            <!-- navigazione -->
            <div class="row vh20  orangeBand justify-content-around align-items-center ">
                <div class=" col-sm-12 col-lg-3"><a class="txtWhite" href="/works">Works</a></div>
                <!-- <div class="col-sm-12 col-lg-3"><a class="txtOrange" href="/about">About</a></div> -->
                <div class=" col-sm-12 col-lg-3"><a class="txtWhite" href="/stack">Stack</a></div>
                <div class=" col-sm-12 col-lg-3"><a class="txtWhite" href="/contacts">Contacts</a></div>
            </div>
        </div>
    </div>
</template>

<script>
// Importa qui i componenti necessari

export default {
    name: 'HomeView', // Cambia il nome del componente con quello desiderato
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
.txt {
    padding: 3rem 0rem;
    line-height: 7rem;
    font-family: Helvetica Neue;
    font-size: 9rem;
    font-weight: bold;
}

.txtWhite {
    font-size: 3rem;
    font-family: Helvetica Neue;
    color: white;
}

.orangeBand {
    background-color: orange;
}

a {
    text-decoration: none;
}

a:hover {
    //-webkit-text-stroke: 3px black;
    transition: color 0.8s;
    color: #212529;
}

img {
    width: 70%;
}

//----------------------------------------------------MEDIA-QUERY---------------------------------------------------------------//
@media only screen and (min-width: 1281px) {
    .txt {
        padding: 5.3rem 3rem;
        line-height: 8rem;
        font-size: 10rem;
    }
}

@media only screen and (min-width: 360px) and (max-width: 768px) {
    // do something in this width range.
}
</style>