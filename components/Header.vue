<template>
  <div>
      <div class="headbar">
        <div class="logo">
          <img src="../assets/axonlogo.png" alt="logo" srcset="">
        </div>
            <div class="headitems">
                <ul>
                    <li v-for="(head,index) in heads" :key="index">
                        <font-awesome-icon :icon="['fas', `${head.icon}`]"/> {{head.text}}
                    </li>
                </ul>
            </div>
      </div>
      <div class="navitems">
        <ul>
            <li v-for="nav in navs" :key="nav.name"><nuxt-link :to="`/${nav.link}`">{{nav.name}}</nuxt-link></li>
        </ul>
      </div>
      <div class="image-bar">
          <h1>Strategy for Norway’s Pesion Fund <br>Global</h1>
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
                text:"'Panthi galli, Pokhara, Nepal"
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
            }
        ],
    }
}
}
</script>

<style scoped>
.logo img{
    max-height: 86px;
    width: auto;
}

.headbar{
    display: flex;
    justify-content: space-around;
}
.headbar ul li{
    color: #1a1e66;
    border-left: 1px solid #d9d9d9;
    border-right: 1px solid #d9d9d9;
    padding: 15px;
}
ul li{
    list-style-type: none;
}
a{
    text-decoration: none;
    color: white;
}

.headitems ul{
    height: 100%;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    min-width: 500px;
}

.navitems{
    background-color: rgb(0, 0, 0,0.7);
}
.navitems ul{
    font-size: 20px;
    font-weight: 600;
    display: flex;
    justify-content: flex-end;
    min-width: 500px;
    padding: 15px 0;
    margin-right: 160px;
}
.navitems ul li{
    margin: 0 10px;
}

.image-bar{
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-image: url("https://previews.123rf.com/images/bialasiewicz/bialasiewicz1706/bialasiewicz170600385/79458613-happy-team-members-clapping-their-hands-in-office.jpg");
    background-size: cover;
    background-position: center;
    background-attachment: scroll;
    min-height: 40vh;
}
.image-bar h1{
    font-size: 3rem;
}
</style>