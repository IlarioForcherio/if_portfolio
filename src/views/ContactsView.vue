<template>
<div>


    
            <section class="section">
                <div class="container">
                    <div class="row">
                        <!-- contact-me-here -->
                        <div class="col-lg-12">
                            <h3  id="contact" class="text-center txt">Contact Me <span style="color:orange">Here</span></h3>
                            <div class="line"></div>
                        </div>
                        <!-- form-contacts -->
                        <div class="col">
                            <form  ref="form" @submit.prevent="sendEmail" class="bw row g-3 text-white p-4">
                                <div class="col-md-6">
                                    <input v-model="name" type="text" name="user_name" placeholder="Name" class="form-control">
                                </div>
                                <div class="col-md-6">
                                    <input v-model='email' type="email" name="user_email" placeholder="Email" class="form-control">
                                </div>
                                <div class="mb-3 col-md-12">
                                    <textarea v-model='message' name="message" placeholder="Message" class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
                                </div>
                                <div class="col-12">
                                    <button value="Send" type="submit" class="btn btn-primary">Send</button>
                                </div>
                                <div class="text-white">{{successEmail}}</div>
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
                    this.successEmail = 'email inviata'
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
.txt{
    padding-top: 100px;
    font-size: 4rem;
}
</style>