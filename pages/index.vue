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
  <TestStructure/>
  <div class="steps-container"></div>
  <div class="empty-container" data-aos="fade-up" data-aos-duration="1500"></div>
</div>
</template>

<script>
import TestStructure from '@/components/TestStructure.vue';
import Navbar from '@/components/Navbar.vue';
import Countries from '@/components/Countries.vue';
export default {
  components:{
    Navbar,
    Countries,
    TestStructure
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
.empty-container{
  height: 100vh;
  background-image: url("https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/02/axon-group-2-scaled.jpg");
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center;
}
.steps-container{
  height: 100vh;
  background-image: url("https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/03/OGA3ET0-scaled.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}
</style>
