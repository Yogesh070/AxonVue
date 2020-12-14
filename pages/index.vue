<template>
<div>
  <div class="container">
      <Navbar/>
    <div class="text-container">
        <p>WELCOME TO</p>
        <h1>AXON Education Consultancy</h1>
        <p>Following are the Countries you can apply for</p>
    </div>
  </div>
  <Countries/>
  <Ielts/>
</div>
</template>

<script>
import Navbar from '@/components/Navbar.vue';
import Countries from '@/components/Countries.vue';
import Ielts from '@/components/Ielts.vue';
export default {
  components:{
    Navbar,
    Countries,
    Ielts
  }
}
</script>

<style scoped>
.container {
  margin: 0 auto;
  min-height: 100vh;
  background-image: url(../assets/homepagebackground.jpg);
  background-position: center;
  background-size: cover;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.text-container{
  margin-bottom: 50px;
  text-align: center;
}
.text-container h1{
  color: #120054;
}
.text-container p{
    letter-spacing: .3em;
    color: #3140fc;
    font-size: 14px;
    font-weight: 600;
    margin-bottom: 13px;
}
</style>
