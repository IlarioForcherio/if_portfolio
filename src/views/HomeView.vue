<template>
    <div>
    
        <div class="container-fluid">
            <!-- intestazione -->
            <div class="row  align-items-center">
                <div class=" col-sm-12 col-lg-6">
                    <div class="title">
                        <h1 class="txt">
                          <span class="" v-for="elem in splitTitle" :key='elem'>{{elem + ' '}}</span>   
                        </h1>
                       
                    </div>
                    
                </div>
                <div class="col-sm-12 col-lg-6">
                    <div class="">
                        <h2 class="bold txtWhite dropIn  text-center"><span style='color:orange'>Ilario</span> Forcherio</h2>
                        <h3 class="bold txtWhite slideFromLeft text-center">Web <span style='color:orange'>Developer</span></h3>
                    </div>
                    <!-- <p class="text-center">"Mi chiamo Ilario e sono un Junior Full Stack Developer. Prima di approdare nel mondo dello sviluppo web ho lavorato molti anni in un settore diverso, fino al momento in cui ho deciso che avrei voluto cambiare vita per accoglierenuove
                            sfide. Il Master Boolean me ne ha dato la possibilita' e ha trasformato in poco tempo una nuova scoperta in una grande passione. Ho imparato a mettermi in gioco e voglio continuare a farlo, quotidianamente e con entusiasmo."</p> -->
                </div>
            </div>
            <!-- navigazione -->
            <div class="row   orangeBand text-center justify-content-around align-items-center ">
                <div class=" col-sm-12 col-lg-3"><a class="txtWhite" href="/works">Works</a></div>
                <!-- <div class="col-sm-12 col-lg-3"><a class="txtOrange" href="/about">About</a></div> -->
                <div class=" col-sm-12 col-lg-3"><a class="txtWhite" href="/stack">Stack</a></div>
                <div class=" col-sm-12 col-lg-3"><a class="txtWhite" href="/contacts">Contacts</a></div>
            </div>
            <div class="d-flex justify-content-center mt-4">
                <div>&#169; Copyright - 2023</div>
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
            title : 'Hi, nice to meet you, my name is',
            splitTitle : '',
        };
    },

    mounted() {
        this.wordsAppear()
    },
    updated() {

    },
    methods: {
        wordsAppear(){
          console.log(this.title) 
          this.splitTitle =  this.title.split(' ');
          console.log(this.splitTitle);
        }

        
       

    }

};
</script>

<style lang="scss" scoped>
.txt {
   
    padding: 3rem 2rem;
    line-height: 7rem;
    font-family: Helvetica Neue;
    font-size: 8rem;
    font-weight: bold; 
}


.txtWhite {
    font-size: 3rem;
    font-family: Helvetica Neue;
    font-weight: bold;
}

.orangeBand {
    background-color: orange;
}

a {
    color: white;
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

.dropIn{
    opacity:0;
     transform: translateY(-200%);
     animation: dropIn 2s forwards;
     animation-delay: 6s;
}
.slideFromLeft{
    opacity:0;
    transform: translateX(-100%);
    animation: slideFromLeft 2s ease forwards; 
    animation-delay: 7s;
}
.txtAppear{

    animation:txtAppear 2s  ease forwards;

}

.orangeBand div{
    opacity: 0;
 animation:txtAppear 2.5s  ease forwards;
}
.orangeBand div:nth-of-type(1){
     animation-delay: 9s;
}
.orangeBand div:nth-of-type(2){
     animation-delay:9.5s;
}
.orangeBand div:nth-of-type(3){
     animation-delay: 10s;
}




//blocco animazione title
.title span{
opacity: 0;
  transform: translateX(-100%);
  animation: slideFromLeft 2.5s ease forwards; 
}

.title span:nth-of-type(1){
    animation-delay: 0.5s;

}
.title span:nth-of-type(2){
    animation-delay: 2s;

}
.title span:nth-of-type(3){
    animation-delay: 2.3s;

}
.title span:nth-of-type(4){
    animation-delay: 2.6s;

}
.title span:nth-of-type(5){
    animation-delay: 2.9s;

}
.title span:nth-of-type(6){
    animation-delay: 4s;

}
.title span:nth-of-type(7){
    animation-delay: 4.5s;

}
.title span:nth-of-type(8){
    animation-delay: 5s;

}







//----------------------------------------------------ANIMATIONS----------------------------------------------------------------//

@keyframes txtAppear{
    from{
        opacity:0
    }
    to {
        opacity:1
    }
}


@keyframes dropIn {
    0% {
        top: -200px;
        opacity: 0;
    }
    50% {
        top: 30%;
        opacity: 1; //transform: rotateX(180deg);
    }
    100% {
        top: 50%;
        opacity: 1;
        transform: rotateX(0deg);
    }
}

@keyframes slideFromLeft {
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

//----------------------------------------------------MEDIA-QUERY---------------------------------------------------------------//
@media only screen and (min-width: 300px) and (max-width: 768px) {
    .txt {
         padding: 0rem;
      
        line-height: 4rem;
        //letter-spacing: -0.2rem;
        text-align: center;
        font-size: 5rem;
    }

    .txtWhite {
    font-size: 2rem;
    
    
    }
}


@media only screen and (min-width: 1281px) and (max-width: 1300px) {
    .txt {
       padding: 4rem;
        line-height: 8rem;
        font-size: 8rem;
    }
}

@media only screen and (min-width: 1301px) and (max-width: 1500px) {
    .txt {
        
       padding: 4rem;
        line-height: 7.8rem;
        font-size: 8.5rem;
    }
}

@media only screen and (min-width: 1500px)  {
    .txt {
        
       padding: 5rem;
        line-height: 8.8rem;
        font-size: 10rem;
    }
}




</style>