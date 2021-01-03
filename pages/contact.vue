<template>
<div>
    <Header title="Contact"/>
    <div class="appointment">
        <h1>Contact our support guys or make appointment with <br> with <i style="color:#3140fc">our consultan</i></h1>
        <div class="appointment-container">
            <div>
                <p>Please contact us using the information below. For additional information on our management consulting services, please visit the appropriate page on our site.</p>
                <p><font-awesome-icon :icon="['fas','map-marker-alt']"/>131 Dartmouth Street</p>
                <p><font-awesome-icon :icon="['fas','phone']"/> +98554466444</p>
                <p><font-awesome-icon :icon="['fas','envelope']"/>Support@mail.com</p>
            </div>
            <ContactForm/>
        </div>
    </div>
    <div class="container">
        <div class="contact">
            <div class="col" v-for="(contact,index) in contacts" :key="index">
                <h1>{{contact.country}}</h1>
                <p style="white-space:pre-wrap;"><font-awesome-icon :icon="['fas','map-marker-alt']"/>{{contact.address}}</p>
                <p><font-awesome-icon :icon="['fas','phone']"/> {{contact.phno}}</p>
                <p><font-awesome-icon :icon="['fas','envelope']"/> {{contact.email}}</p>
            </div>
        </div>
    </div>
</div>
</template>

<script>
import Header from '@/components/Header.vue';
import ContactForm from '@/components/ContactForm.vue';
export default {
    components:{
        Header,
        ContactForm,
    },
    data(){
        return{
            contacts:[
                {
                    country:"Australia",
                    phno:"+1-(281)-813 926+1-(281)-813 612",
                    address:"49488 Avenida Obregon,La Quinta, CA 92253",
                    email:"support@finan.com.aus"
                },
                {
                    country:"Netherlands",
                    phno:"+1-(281)-813 926+1-(281)-813 612",
                    address:"13/1 Dixon Street, SydneyNSW 2000",
                    email:"support@finan.com.nether"
                },
                {
                    country:"United Kingdom",
                    phno:"+1-(281)-813 926+1-(281)-813 612",
                    address:"49488 Avenida Obregon,La Quinta, CA 92253",
                    email:"support@finan.com.uk"
                },
            ]
        }
    }
}
</script>

<style scoped>
.contact{
    display: flex;
    /* justify-content: center; */
    justify-content: space-around;
    background-image: url("https://images.pexels.com/photos/187913/pexels-photo-187913.jpeg");
    background-position: center;
    background-size: cover;
    color: white;
    padding: 80px 147px;
}
.contact p{
    font-weight: 500;
    margin: 15px;
}
.appointment{
    color: #1a1e66;
    min-height: 60vh;
    padding: 70px 90px;
    background-color: #f2f3fa;
}
.appointment-container p{
    margin: 15px;
}
.appointment .appointment-container{
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.appointment-container{
    flex-wrap: wrap;
}
.appointment-container>div{
    max-width: 40%;
}

@media only screen and (max-width: 600px) {
  .appointment-container>div{
    max-width: 100%;
}
.appointment{
    padding: 0;
}
}
</style>