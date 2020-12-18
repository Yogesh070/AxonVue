<template>
<div>
  <div class="container">
        <div class="contacts">
            <ul>
                <li>+977 9816162091 / 9802821038</li>
                <li>mail@axon.edu.np</li>
                <li>Panthi Galli,Pokhara 33700</li>
            </ul>
            <div>
                <img src="../assets/axonlogo.png" alt="logo" srcset="">
            </div>
      </div>
      <div class="links">
          <h2>Links</h2>
          <ul>
              <li v-for="nav in navs" :key="nav.name"><nuxt-link :to="`/${nav.link}`">{{nav.name}}</nuxt-link></li>
          </ul>
      </div>
      <div class="gallery">
          <h2>Gallery</h2>
          <div class="socials">
              <h2>Find us at</h2>
              <ul>
                  <li v-for="social in socials" :key="social.name"><a :href="social.link"><img :src="'/_nuxt/assets/'+ social.name" :alt="social.name"></a></li>
              </ul>
          </div>
      </div>
  </div>
       <div class="copyright">
          <div>
              <p>2020 © All rights reserved by Axon Education</p>
          </div>
          <div><p>Find us at:<a v-for="social in socials" :key="social.name" :href="social.link">{{social.name}}</a></p></div>   
      </div>
</div>
</template>

<script>
export default {
data(){
    return{
        socials:[
            {
                name:"fb.png",
                link:"www.facebook.com"
            },
            {
                name:"insta.png",
                link:""
            },
            {
                name:"twitter.png",
                link:""
            },
        ],
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
            },
        ]
    }
}
}
</script>

<style scoped>
a{
    text-decoration: none;
    color: #afd3f3;
}
.container{
    display: flex;
    justify-content: space-around;
    /* align-items: center; */
    background-color: #1a1e66;
    padding: 80px;
}
ul li{
    list-style-type: none;
    color: #afd3f3;
    margin-top: 15px;
}
ul li:hover{
    color: white;
    text-decoration: underline;
}
ul{
    padding: 0;
}
h2{
    color: white;
}
img{
    max-height: 86px;
    margin-top: 50px;
}
.gallery{
    display: flex;
    flex-direction: column;
    justify-content: space-around;
}
.socials ul{
    display: flex;
    justify-content: space-between;
}
.socials ul li{
    margin-right:10px;
}
.copyright{
    display: flex;
    justify-content: space-around;
    background-color: #020f2f;
    color: white;
    padding: 10px 0;
}
.copyright a{
    margin: 0 10px;
}
</style>