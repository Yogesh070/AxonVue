<template>
  <div class="navbar">
      <div class="logo">
          <img src="../assets/axonlogo.png" alt="logo" srcset="">
      </div>
      <div class="navitems">
        <ul>
            <li v-for="nav in navs" :key="nav.name"><nuxt-link :to="`/${nav.link}`">{{nav.name}}</nuxt-link></li>
        </ul>
      </div>
  </div>
</template>

<script>
export default {
data(){
    return{
        navs:[
            {
                name:"Home",
                link:""
            },
            {
                name:"About Us",
                link:"about"
            },
             {
                name:"Blog",
                link:"blog"
            },
             {
                name:"Contact",
                link:"contact"
            }
        ]
    }
}
};
</script>

<style scoped>
a{
    text-decoration: none;
    color: white;
}
.logo{
    background-color: white;
    padding: 31px 27px 52px;
    border-radius: 0 0 76px 76px;
}
.logo img{
    max-height: 86px;
    width: auto;
}
.navbar{
    display: flex;
    justify-content: space-around;
}
ul li{
    list-style-type: none;
}
.navitems ul{
    height: 100%;
    font-size: 20px;
    font-weight: 600;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    min-width: 500px;
}
</style>