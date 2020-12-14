<template>
<div>
  

  <div class="container">
    <div class="text-content">
      <h1>IELTS test structure</h1>
      <p>
        IELTS consists of four parts: Listening, reading, Writing and Speaking.
        Listening and Speaking are the same in both general training and
        academic versions of the exam.
      </p>
      <p>The total test duration is 2 hours and 45 minutes.</p>
      <p>After all four sections are completed; you are done with your exam.</p>
      <button>Read More</button>
    </div>
    <div class="box">
      <div class="card" v-for="item in ielts" :key="item">
        <div v-for="content in item.type" :key="content">
          <img  :src="content.image" :alt="content.name">
          <h2>{{content.name}}</h2>
          <p v-for="text in content.content" :key="text">{{text}}</p>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  data() {
    return {
      ielts: [
        {
          type: [
            {
              name: "Listening",
              image:
                "https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/02/wr.png",
              content: ["40 Dialogues", "40 Minutes"],
            },
          ],
        },
        { type: [
            {
              name: "Writing",
              image:
                "https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/02/write.png",
              content: ["3 Texts, 40 Questions", "60 minutes"],
            },
          ],
          },
          {
             type: [
            {
              name: "Reading",
              image:
                "https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/02/Read.png",
              content: ["Describing Graph + Essay", "60 Minutes"],
            },
          ],
          },
          {
            type: [
            {
              name: "Speaking",
              image:
                "https://cdn.statically.io/img/axon.edu.np/f=auto%2Cq=80/wp-content/uploads/2020/02/Speak.png",
              content: ["3 Dialogues", "15 Minutes"],
            },
          ],
        },
      ],
    }
  },
};
</script>

<style scoped>
.text-content{
    padding: 50px;
    display: flex;
    flex-direction: column;
    align-items: center;
    color: #1a1e66;
}
.container {
  display: flex;
  padding: 0 80px;
}
.box{
  display: flex;
  flex-wrap: wrap;
}
.card {
  background-color: white;
  color: #1a1e66;
  box-shadow: 0 1px 18px rgba(0, 0, 0, 0.11);
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  min-height: 270px;
  min-width: 270px;
  padding: 47px 30px;
  margin: 20px;
}
.card:hover {
  background-image: linear-gradient(to top, #f44c01, #ff7a01);
  transition: all 300ms linear 0ms;
}
p{
  margin-bottom: 25px;
  line-height: 1.625;
}
h1{
  margin-bottom: 55px;
}
button{
    background-color: #4659e2;
    color: white;
    box-shadow: 0 2px 4px rgba(0,0,0,.1) inset;
    font-size: 14px;
    padding: 11px 35px;
    box-shadow: none;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}
button:hover{
  opacity: 0.8;
}
</style>
