<template>
  <div>
    <div class="container">
      <h1>Test Structure Overview</h1>
      <div class="options-panel">
        <button v-for="tab in edupackage" :key="tab.title"  v-bind:class="['tab-button', { active: currentTab === tab }]"
        v-on:click="currentTab = tab">{{tab.toUpperCase()}} </button>
      </div>
    </div>
    <component :is="currentTabComponent" class="tab"></component>
  </div>
</template>

<script>
import Ielts from '@/components/Ielts.vue';
import Tofel from '@/components/Tofel.vue';
import Pte from '@/components/Pte.vue';
import Gre from '@/components/Gre.vue';
export default {
data(){
  return{
    currentTab: "Ielts",
    edupackage:['Ielts','Tofel','Gre','Pte','Sat','Gmat'],
  }
},
computed: {
  currentTabComponent: function() {
  return this.currentTab;
  }
},
components:{
  Ielts,
  Tofel,
  Pte,
  Gre,
},
}
</script>

<style scoped>
.container{
  min-height: 60vh;
  background-image: url("https://www.thestatesman.com/wp-content/uploads/2018/10/study-abroad.jpg");
  background-size: cover;
  display: flex;
  align-items: center;
  color: white;
  /* background-position: center; */
  position: relative;
}
.options-panel{
  display: grid;
  grid-template-columns: repeat(6,1fr);
  gap: 20px;
  justify-items: center;
  width: 100%;
  position: absolute;
  bottom: 0;
  grid-auto-rows: minmax(50px, auto);
}
.tab-button {
  background-color: #4659e2;
  color: white;
  box-shadow: 0 2px 4px rgba(0,0,0,.1) inset;
  border: none;
  border-radius: 4px 4px 0 0;
  cursor: pointer;
  font-size: 16px;
  outline: none;
  min-width: 130px;
}
.tab-button:hover {
  background-color: white;
  color:#4659e2;
}
.tab-button.active {
  background-color: white;
  color: #4659e2;
}
.tab {
  border: 1px solid #ccc;
  padding: 10px;
}

h1 {
    font-weight: 900;
    font-size: 40px;
    margin-left: 100px;
}
@media only screen and (max-width: 900px) {
  .options-panel{
  grid-template-columns: repeat(3,1fr);
  gap: 10px;
}
}
</style>