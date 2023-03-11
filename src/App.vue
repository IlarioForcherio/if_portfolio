<template>
    <div id='app'>
        <header>    
                    <!-- <router-link to="/">Home</router-link> 
                    <router-link to="/about">About</router-link> -->
            <nav class="navbar navbar-expand-lg shadow-lg bg-body-tertiary rounded">
                <div class="container-fluid d-flex justify-content-between">
                    <a class="navbar-brand" href="/"><i class="fa-solid fa-house"></i></a>
                    <button class="navbar-toggler ms-5" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
            </button>
                    <div class="collapse navbar-collapse" id="navbarNav">
                        <ul class="navbar-nav">
                            <li class="nav-item">
                                <!-- <a class="nav-link" aria-current="page" href="/"><i class="fa-solid fa-house"></i></a> -->
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="/works" >Works</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="/stack" >Stack</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="/contacts" >Contacts</a>
                            </li>
                        </ul>
                    </div>
    
                    <!-- switch -->
                    <div class="form-check form-switch">
                        <div class="form-check form-switch">
                            <input @click="toggleDarkMode" class="form-check-input" type="checkbox" role="switch" id="flexSwitchCheckDefault">
                            <label class="form-check-label" for="flexSwitchCheckDefault"></label>
                            <i :class="['fa-regular','fa-moon' ,  this.isDarkMode ? 'd-none' : 'd-block' ]"></i>
                            <i :class="['fa-regular','fa-sun' ,  !this.isDarkMode ? 'd-none' : 'd-block' ]"></i>
                        </div>
     
                    </div>
                </div>
            </nav>
        </header>
    <!-- router -->
        <router-view></router-view>


    </div>
</template>

<script>
export default {
    name: 'App', // Cambia il nome del componente con quello desiderato
    components: {
        // HeaderComp
    },
    props: {

    },
    data() {
        return {
            toggle: '',
            isDarkMode: false,
        };
    },
    beforeUpdate() {
        localStorage.setItem('isDarkMode', this.isDarkMode)
    },

    mounted() {
        this.isDarkMode = localStorage.getItem('isDarkMode') !== 'false' ? true : false;
    },
    watch: {
        isDarkMode() {
            const htmlElement = document.querySelector('html')
            htmlElement.setAttribute('data-bs-theme', this.isDarkMode ? 'dark' : 'light')
        }
    },
    methods: {


        toggleDarkMode() {
            this.isDarkMode = !this.isDarkMode
        }




    },
};
</script>

<style lang="scss">
#app {
    // height: 100vh; // background-color: #2b3035;
    font-family: Avenir, Helvetica, Arial, sans-serif; // -webkit-font-smoothing: antialiased;
    // -moz-osx-font-smoothing: grayscale;
    // text-align: center;
    // color: #2c3e50;
}
header{
     width: 100%;
    position: sticky;
    z-index: 2;
    top: 0;
    // background-color: rgba(0, 0, 0, 0.3) !important;
}

nav {

    background-color: rgba(33, 37, 41, 0.2) !important;
}


* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

#icon:hover {
    transform: scale(1.1);
}

#icon:active {
    transform: scale(1);
}

//toggle checkbox
.form-switch {
    position: relative;
}

.fa-moon {
    font-size: 0.8rem;
    position: absolute;
    left: 10%;
    top: 24%;
}

.fa-sun {
    top: 30%;
    right: 30%;
    font-size: 0.6rem;
    position: absolute;
}
</style>







