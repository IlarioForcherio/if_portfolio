<template>
    <div class="timeLine">
      <h3  id="contact" class="p-5 text-center txt">This is my <span style="color:orange">Stack</span></h3>
        <!-- left -->
        <div class=" d-flex justify-content-center">
          
            <div class="left d-flex flex-column">
                <div class="pt-4"><img src="../assets/img/icons8-html-5-48.png" alt=""></div>
                <div class="pt-4"><img src="../assets/img/icons8-bootstrap-48.png" alt=""></div>
                <div class="pt-4"><img src="../assets/img/icons8-vue-js-48.png" alt=""></div>
                <div class="pt-4"><img src="../assets/img/icons8-my-sql-48.png" alt=""></div>
                <div class="pt-4"><img src="../assets/img/icons8-php-48.png" alt=""></div>
                <div class="pt-4"><img src="../assets/img/icons8-visual-studio-48.png" alt=""></div>
            </div>
    
            <div class="middleLine d-flex flex-column align-items-center">
                <div class="circle"></div>
                <div class="hLine "></div>
                <div style='color:orange' class="text-center"> <i class="fa-solid fa-chevron-down"></i></div>
            </div>
    
            <!-- right -->
            <div class="right d-flex flex-column">
                <div class="pt-5"><img src="../assets/img/icons8-css3-48.png" alt=""></div>
                <div class="pt-5"><img src="../assets/img/icons8-javascript-48.png " alt=""></div>
                <div class="pt-5"><img src="../assets/img/icons8-npm-48.png" alt=""></div>
                <div class="pt-5"><img src="../assets/img/icons8-git-48.png" alt=""></div>
                <div class="pt-5"><img style="width:80%" src="../assets/img/985px-Laravel.png" alt=""></div>
    
            </div>
        </div>
    </div>
</template>

<script>
// Importa qui i componenti necessari

export default {
    name: 'StackView', // Cambia il nome del componente con quello desiderato
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
    font-weight: bold;
    
}
ul {
    padding: 0px;
    list-style: none;
}

.line {
    width: 90%; //border: 1px solid white;
}

.hLine {
    margin: 0px 10px;
    border: 1px solid orange;
    height: 500px;
    width: 1px;
}

.circle {
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background-color: orange;
}

.space {
    border: 1px solid white;
    height: 0px;
    width: 50px;
}
.img {
    //margin-left: 100px;
    //width: 100px;
    // height: 100px;
    //border-radius: 50%;
    border: 1px solid white;
}

.middleLine {
    transform: translateY(-200%);
    animation: dropIn 2s forwards;
}

img {
    //float: left;
    //aspect-ratio: 1/1;
    //object-fit: cover;
    width: 100%; // border-radius: 50%;
    // border: 1px solid white;
}


// blocco selettori 'left'


.left  img {
  opacity: 0;
  transform: translateX(-100%);
  animation: slideFromLeft 0.5s ease forwards;
}
.left div:nth-of-type(1) img:nth-of-type(1) {
  animation-delay: 1s;
}

.left div:nth-of-type(2) img:nth-of-type(1) {
  animation-delay: 1.2s;
}

.left div:nth-of-type(3) img:nth-of-type(1) {
  animation-delay: 1.4s;
}
.left div:nth-of-type(4) img:nth-of-type(1) {
  animation-delay: 1.6s;
}

.left div:nth-of-type(5) img:nth-of-type(1) {
  animation-delay: 1.8s;
}

.left div:nth-of-type(6) img:nth-of-type(1) {
  animation-delay: 2s;
}

// blocco selettori 'right'

.right  img {
  opacity: 0;
  transform: translateX(100%);
  animation: slideFromLeft 0.5s ease forwards;
}
.right div:nth-of-type(1) img:nth-of-type(1) {
  animation-delay: 1s;
}

.right div:nth-of-type(2) img:nth-of-type(1) {
  animation-delay: 1.2s;
}

.right div:nth-of-type(3) img:nth-of-type(1) {
  animation-delay: 1.4s;
}
.right div:nth-of-type(4) img:nth-of-type(1) {
  animation-delay: 1.6s;
}

.right div:nth-of-type(5) img:nth-of-type(1) {
  animation-delay: 1.8s;
}

.right div:nth-of-type(6) img:nth-of-type(1) {
  animation-delay: 2s;
}


//--------------------------------------------ANIMATION--------------------------------------------------//
//freccia dall'alto
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
//icone da sinistra

@keyframes slideFromLeft {
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

//----------------------------------------------------MEDIA-QUERY---------------------------------------------------------------//
@media only screen and (min-width: 300px) and (max-width: 768px) {
    .txt {
        font-size: 3rem;
    }
}
</style>