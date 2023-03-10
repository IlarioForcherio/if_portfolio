<template>
    <div>
       <header class="vh10">
            <!-- <router-link to="/">Home</router-link> 
                            <router-link to="/about">About</router-link> -->
            <nav class="navbar navbar-expand-lg bg-body-tertiary">
                <div class="container-fluid">
    
                    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                                <span class="navbar-toggler-icon"></span>
                            </button>
                    <div class="collapse navbar-collapse justify-content-between" id="navbarNavAltMarkup">
                        <div class="navbar-nav">
                            <!-- <router-link to="/">Home</router-link>  -->
                            <a class="nav-link" aria-current="page" href="/">Home</a>
                            <a class="nav-link" href="/works">Works</a>
                            <!-- <a class="nav-link" href="/about">About</a> -->
                            <a class="nav-link" href="/stack">Stack</a>
                            <a class="nav-link" href="/contacts">Contacts</a>
                        </div>
                        <!-- switch -->
                        <div class="form-check form-switch">
                            <!-- <i id="icon" @click="toggleDarkMode" :class="'fa-solid fa-circle-half-stroke'"></i> -->
                           
                            <div class="form-check form-switch">
                                <input @click="toggleDarkMode" class="form-check-input" type="checkbox" role="switch" id="flexSwitchCheckDefault">
                                <label class="form-check-label" for="flexSwitchCheckDefault"></label>
                                <i :class="['fa-regular','fa-moon' ,  this.isDarkMode ? 'd-none' : 'd-block' ]"></i>
                                <i :class="['fa-regular','fa-sun' ,  !this.isDarkMode ? 'd-none' : 'd-block' ]"></i>
                                
                            </div>
                             

                        </div>
                    </div>
                </div>
            </nav>
        </header>
    
    </div>
</template>

<script>
// Importa qui i componenti necessari

export default {
    name: 'HeaderComp', // Cambia il nome del componente con quello desiderato
    components: {
        // Aggiungi qui i componenti importati
    },
    props: {

    },
    data() {
        return {
            isDarkMode: false,
        };
    },

    mounted() {

    },
    methods: {
         toggleDarkMode() {
            this.isDarkMode = !this.isDarkMode
            
            this.$emit('emitIsisDarkMode', this.isDarkMode);
        }
        


    },
};
</script>

<style lang="scss" scoped>
.vh10{
    height:10vh;
}
// .fa-circle-half-stroke {
//     color: white;
// }

// .cb {
//     color: black;
// }


#icon:hover {
    transform: scale(1.1);
}

#icon:active {
    transform: scale(1);
}
//toggle checkbox

.form-switch{
   position: relative;
   
}
.fa-moon{
font-size: 0.8rem;
position: absolute;
left:10%;
top:20%;

}
.fa-sun{
    top:30%;
    right: 30%;
    font-size: 0.6rem;
   position: absolute;  
}
</style>