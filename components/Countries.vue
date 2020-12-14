<template>
<div class="parent">
    <div class="card" v-for="item in country" :key="item.name">
        <div>
            <img :src="item.image" :alt="item.name" srcset="">
            <h3>{{item.name.toUpperCase()}}</h3>
        </div>
    </div>
    
</div>
  
</template>

<script>
export default {
data(){
    return{
        country:[{
            name:"USA",
            image:"https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/02/USA.png"
        },
        {
            name:"UK",
            image:"https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/02/UK.png"
        },
        {
            name:"Austalia",
            image:"https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/02/Australia-e1581508839222.png"
        },
        {
            name:"New zealand",
            image:"https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/02/Newzealand.png"
        },
        {
            name:"Canada",
            image:"https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/02/Canada.png"
        },
        {
            name:"Cyprus",
            image:"https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/02/Cyprus.png"
        },
        {
            name:"Japan",
            image:"https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/02/Japan.png"
        },
        {
            name:"Plillipines",
            image:"https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/02/Phillipines.png"
        },
        {
            name:"Poland",
            image:"https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/02/Poland.png"
        },
        {
            name:"Hungary",
            image:"https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/02/Hungary-1-e1581505776347.png"
        },
        
        ]
    }
}
}
</script>

<style scoped>
.parent{
    min-height: 100vh;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    padding: 0 80px;
}
.card{
    padding: 47px 30px;
    max-height: 280px;
    background-color: white;
    box-shadow: 0 1px 18px rgba(0,0,0,.11);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    margin: 20px;
}
.card:hover{
    background-image: linear-gradient(to top,#f44c01,#ff7a01);
    transition: all 300ms linear 0ms;
}
.card img{
    height: 130px;
    width: 130px;
}
.card h3{
    margin-top: 18px;
    color: #3140fc;
}
</style>