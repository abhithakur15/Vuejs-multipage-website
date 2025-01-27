<template>
<section class="team">
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-6 ">
        <div class="text-center set-text">
            <MainTitle text="Our Team" text1="Meet With Our Expert
Team"></MainTitle>
          </div>
      </div>
    </div>
    <div class="row">
      <div class="col-lg-3 col-sm-6 col-md-6 mb-2" v-for="(data, index) in data1" :key="index">
        <div class="team-a">
          <div class="team-box">
          <img :src="require(`@/assets/images/${data.path}.png`)" alt="" class="img-fluid">
        </div>
        <div class="team-text mt-3">
          <div class="text-center">
            <h4 class="text-white">{{ data.text }}</h4>
            <p class="text-white">{{ data.text1 }}</p>
          </div>
    
        </div>
        </div>
     
      </div>
    </div>
  </div>
</section>
  </template>
  <script>
import MainTitle from '@/components/MainTitle.vue';

  export default {
    name: 'HomeView',
    components: {
      MainTitle
    },
    data() {
    return {
    
      data1: [
        {
        path: "team1",
        text:"John Doe",
             text1:"CEO & Founder"
      },
      {
        path: "team2",
              text:"Jane Smith",
                  text1:"Chef Technology Officer"
      },
      {
        path: "team3",
              text:"Sarah Thompson",
                  text1:"Head of Project Management"
      },
      {
        path: "team4",
              text:"David Garcia",
                  text1:"Lead Software Engineer"
      },
      {
        path: "team5",
              text:"David Garcia",
                  text1:"Lead Software Engineer"
      },
      {
        path: "team6",
              text:"David Garcia",
                  text1:"Lead Software Engineer"
      },
      {
        path: "team7",
              text:"David Garcia",
                  text1:"Lead Software Engineer"
      },
      {
        path: "team8",
              text:"David Garcia",
                  text1:"Lead Software Engineer"
      }
    ]
    };
  }
  }

</script>
  <style scoped>

.team {
  padding: 50px 0 100px 0;
}
</style>