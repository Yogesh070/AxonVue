<template>
  <div>
      <div class="container">
          <div class="top-container">
            <div class="card" data-aos="fade-up" data-aos-duration="3000" v-for="card in cards" :key="card.title">
                <h2>{{card.title}}</h2>
                <p>{{card.text}}</p>
            </div>
          </div>
          <div class="mid-container">
              <span >ABOUT US</span>
              <h1>We are here to manage your finance <br> with <i style="color:#3140fc">experience</i> </h1>
              <div class="mid-content" data-aos="fade-right" data-aos-duration="500" data-aos-offset="300" data-aos-easing="ease-in-sine">
              <div class="img-container">
                  <img src="https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2018/12/banner1.jpg" alt="client">
              </div>
                <div class="content">
                    <div class="progress" v-for="item in progress" :key="item.title">
                        <h2>{{item.title}}</h2>
                        <div :style="{width: item.percentage + '%'} " class="progress-bar">
                            <span>{{item.percentage}}</span>
                        </div>
                    </div>
                    <p>The argument in favor of using filler text goes something like this: If you use real content in the design process, anytime you reach a review point you’ll end up reviewing and negotiating the content itself and not the design.
                    </p>
                    <p>
                    Aenean tincidunt id mauris id auctor. Donec at ligula lacus. Nulla dignissim mi quis neque interdum, quis porta sem finibus.
                    </p>
                </div>
              </div>
          </div>
          <div class="video">
                <span>VIDEO</span>
                <h1>See how we work with <br> touch of <i>experience</i></h1>
              <button data-aos="fade-up" data-aos-duration="3000"><a href="https://www.youtube.com/" target="_blank">Play</a></button>
          </div>
          <ChooseUs/>
          <div class="help">
              <h1 style="color:white">Find out where to get free <i style="color:#3140fc">help now!</i> </h1>
              <button>Request Now</button>
          </div>
      </div>
  </div>
</template>

<script>
import ChooseUs from '@/components/ChooseUs.vue';
export default {
    components:{
        ChooseUs,
    },
    data(){
        return{
            progress:[{
                title:'Finance',
                percentage:'95'
            },
            {
                title:'Business',
                percentage:'90'
            },
            {
                title:'Investment',
                percentage:'93'
            },],
            cards:[
                {
                    title:"Business Growth",
                    text:"The argument in favor of using filler text goes some labore et dolore magna aliqua consectetur."
                },
                {
                    title:"Strategy Process",
                    text:"The argument in favor of using filler text goes some labore et dolore magna aliqua consectetur."
                },
                {
                    title:"Finance Manage",
                    text:"The argument in favor of using filler text goes some labore et dolore magna aliqua consectetur."
                },
            ]
        }
    }

}
</script>

<style scoped>
.top-container{
    display: flex;
    justify-content: center;
    min-height: 60vh;
    align-items: center;
    padding: 0 145px;
    background-color: #f2f3fa;
}
.card{
    background-color: white;
    text-align: center;
    padding: 40px 20px;
    margin: 0 15px;
    min-height: 250px;
}
.card h2{
    line-height: 1.625;
    color: #1a1e66;
    
}
.card h1:hover{
    color: #3140fc;
}

.card p{
    margin-top: 20px;
    color: #3140fc;
}
.card:hover{
    transform: translateY(30px);
    transition: transform 1s ease ;
    border-bottom: 4px solid #1a1e66; ;
}
h1{
    color: #1a1e66;
}
.mid-container{
    text-align: center;
    margin: 35px 0;
}
.mid-content{
    display: flex;
    width: 100%;
    align-items: center;
    justify-content: center;
    text-align: left;
    padding: 65px;
}
.content{
    max-width: 50%;
    margin-left: 50px;
    color: #1a1e66;
}
.content p{
    margin-bottom: 26px;
}

.progress h2{
    font-size: 18px;
    line-height: 1.625;
    margin-bottom: 9px;
}
.progress-bar{
    border-bottom: 3px solid black;
    margin: 20px 0;
    position: relative;
}
.progress-bar span{
    position: absolute;
    right: 0;
    padding: 15px 18px;
    color: white;
    font-weight: 700;
    background-color: #1a1e66;
    border-radius: 50%;
    top: -30px;
}
.video{
    text-align: center;
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-image: url("https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NHx8b2ZmaWNlfGVufDB8fDB8&ixlib=rb-1.2.1&w=1000&q=80");
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
    min-height: 60vh;
    
}
.video button{
    border: none;
    border-radius: 50%;
    padding: 25px 20px;
    background-color: #3140fc;
    outline: none;
    cursor: pointer;
}
.video button a{
    text-decoration: none;
    color: white;
}
.help{
    display: flex;
    justify-content: space-around;
    padding: 13px 0;
    background-color: #020f2f;
}
.help button{
    background-color: white;
    padding: 0 17px;
    border-radius: 6px;
    outline: none;
    cursor: pointer;
}
</style>