<template>
<div>
  <div class="container">
        <div class="contacts">
            <ul>
                <li v-for="(head,index) in heads" :key="index">
                    <font-awesome-icon :icon="['fas', `${head.icon}`]"/> {{head.text}}
                </li>
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
                  <li v-for="social in socials" :key="social.name"><a :href="social.link" target="_blank"><font-awesome-icon :icon="['fab', `${social.name}`]"/></a></li>
              </ul>
          </div>
      </div>
  </div>
       <div class="copyright">
          <div>
              <p>2020 © All rights reserved by Axon Education</p>
          </div>
          <div><p>Find us at:<a  v-for="social in socials" :key="social.name" :href="social.link" target="_blank"><font-awesome-icon :icon="['fab', `${social.name}`]"/></a></p></div>   
      </div>
</div>
</template>

<script>
export default {
data(){
    return{
        heads:[
            {
                icon:"envelope",
                text:"mail@axon.edu.np"
            },
            {
                icon:"phone",
                text:"061527146, 9805821350"
            },
            {
                icon:"map-marker-alt",
                text:"Panthi galli, Pokhara, Nepal"
            },
        ],
        socials:[
            {
                name:"facebook",
                link:"http://www.facebook.com"
            },
            {
                name:"instagram",
                link:"http://www.instagram.com"
            },
            {
                name:"twitter",
                link:"http://www.twitter.com"
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
    padding: 80px 0;
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
    /* justify-content: space-around; */
}
.socials ul{
    display: flex;
    justify-content: space-between;
}
.socials ul li{
    margin-right:10px;
    font-size: 32px;
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

.fa-instagram{
    color: #E1306C;
}
.fa-twitter{
    color: #1DA1F2;
}
.fa-facebook{
    color: white;
}
</style>