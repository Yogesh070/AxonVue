<template>
<div>
  <div class="container">
      <div class="top-container">
          <div>
              <span>WHY CHOOSE US</span>
            <h1>There are many companies but <br> why  <i style="color:#3140fc">choose us</i></h1>
          </div>
            <p>The argument in favor of using filler text goes something like this: If you use real content in the design process, anytime you reach a review point you’ll end up reviewing and negotiating the content itself and not the design.
            </p>
      </div>
      <div class="main-container">
              <div class="card-container" :class="{active:activeCard}">
                  <div class="card" v-for="card in cards" :key="card.title" @click="displayImage(card.image)">
                    <h2>{{card.title}}</h2>
                    <p>{{card.text}}</p>
                </div>
              </div>
            <div class="img-container">
                <img :src="activeImage" alt="people">
            </div>
      </div>
  </div>
</div>

</template>

<script>
export default {
    data(){
        return{
            activeImage:'https://st.depositphotos.com/1743476/1224/i/600/depositphotos_12243165-stock-photo-business-handshake-to-seal-a.jpg',
            activeCard:false,
            cards:[
                {
                    title:"Expert team",
                    text:"The argument in favorite of using filler to text goes some thing like this top",
                    image:"https://st.depositphotos.com/1743476/1224/i/600/depositphotos_12243165-stock-photo-business-handshake-to-seal-a.jpg"
                },
                 {
                    title:"Best Finance Brand",
                    text:"The argument in favorite of using filler to text goes some thing like this top",
                    image:"https://thumbs.dreamstime.com/b/happy-diverse-office-workers-team-laughing-together-group-meeting-cheerful-funny-joke-work-corporate-business-excited-smiling-141680673.jpg"
                },
                 {
                    title:"Best Leadership Ideas",
                    text:"The argument in favorite of using filler to text goes some thing like this top",
                    image:"https://previews.123rf.com/images/chagin/chagin1203/chagin120300202/12836611-business-people-in-modern-office.jpg"
                },
            ]
        }
    },
    methods:{
        displayImage(i){
            this.activeImage=i;
        }
    }

}
</script>

<style scoped>
.container{
    margin: 60px 0;
}
.top-container p{
    max-width: 525px;
}
.top-container h1{
    color: #1a1e66;
}
.top-container,.main-container{
    display: flex;
    justify-content: space-evenly;
    align-items: center;
}
.card{
    margin: 10px 0;
    border: 1px solid #d9d9d9;
    padding: 25px;
    cursor: pointer;
    max-width: 400px;
}
.img-container img{
    max-width: 660px;
    max-height: 440px;
    object-fit: cover;
}
.card p{
    color: #666;
}
.active{
    background-color: #1a1e66;
}
</style>