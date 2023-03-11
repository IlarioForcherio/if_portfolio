<template>
    <div>
    
    
    
        <section class="section">
            <div class="container">
                <div class="row">
                    <!-- contact-me-here -->
                    <div class="col-lg-12">
                        <h3 id="contact" class="text-center txt">Contact Me <span style="color:orange">Here</span></h3>
                        <div class="line"></div>
                    </div>
                    <!-- form-contacts -->
                    <div class="col">
                        <form ref="form" @submit.prevent="sendEmail" class="bw row g-3 text-white p-4">
                            <div class="col-md-6">
                                <input v-model="name" type="text" name="user_name" placeholder="Name" class="form-control">
                            </div>
                            <div class="col-md-6">
                                <input v-model='email' type="email" name="user_email" placeholder="Email" class="form-control">
                            </div>
                            <div class="mb-3 col-md-12">
                                <textarea v-model='message' name="message" placeholder="Message" class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
                            </div>
                            <div class="col-12 d-flex justify-content-between align-items-center">
                                <button value="Send" type="submit" class="btn btn-primary">Send</button>
                                <div>
                                <a href="https://www.linkedin.com/in/ilario-forcherio-b413a340/"><i class="m-3 fa-brands fa-linkedin"></i></a>
                                <a href="https://github.com/IlarioForcherio"><i class="m-3 fa-brands fa-square-github"></i>  </a>
                                </div>
                                
                            </div>
                            <div class="alert"></div>
                            <div v-if='success' class="alert alert-success" role="alert">
                                {{successEmail}}
                            </div>
                        </form>
   
                    </div>
    
                </div>
            </div>
            <!-- icons-email -->
    
    
    
        </section>
    
    
    </div>
</template>

<script>
import emailjs from '@emailjs/browser'

export default {
    name: 'ContactsView', // Cambia il nome del componente con quello desiderato
    components: {
        // Aggiungi qui i componenti importati
    },
    props: {

    },
    data() {
        return {
            successEmail: '',
            name: '',
            email: '',
            message: '',
            success:false,
        };
    },

    mounted() {
        // Inserisci qui il codice da eseguire quando il componente viene montato
    },
    methods: {
        sendEmail() {
            emailjs.sendForm('service_op7yte9', 'template_ba097v6', this.$refs.form, 'yQKnIfUJ2g1UJVw-B')
                .then((result) => {
                    console.log('SUCCESS!', result.text)
                    this.success = true;
                    this.successEmail = 'Email inviata con successo'
                    this.name = '',
                        this.email = '',
                        this.message = ''

                }, (error) => {
                    console.log('FAILED...', error.text);
                });
        }
    },
};
</script>

<style lang="scss" scoped>
a{
     color: orange;
   font-size: 2rem;
    text-decoration: none;
   
}
a:hover{
 transition: color 0.8s;
    color: white;
}


button{
    color: orange;
    background-color: #212529;
    border: 1px solid orange;
}
button:hover{
   border: 1px solid orange;
    color: white;
    background-color: orange;
}

.txt {
    padding-top: 100px;
    font-size: 4rem;
    font-weight: bold;
}
//----------------------------------------------------MEDIA-QUERY---------------------------------------------------------------//
@media only screen and (min-width: 300px) and (max-width: 768px) {
    .txt {
        font-size: 3rem;
    }
}
</style>