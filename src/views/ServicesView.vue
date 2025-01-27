<template>
 <section class="our_services_detail">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-8">
          <div class="text-center set-text">
            <MainTitle text="Our Service" text1="Empower Your Business with Our
Comprehensive IT Solutions"></MainTitle>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-lg-4 col-sm-6 col-md-6 my-3 " v-for="(data, index) in data" :key="index">
          <div class="card-b h-100">
            <div class="icon-box">
              <img :src="require(`@/assets/images/${data.path}`)" alt="" class="img-fluid">
            </div>
            <div class="text-box">
              <h5 class="text-white">{{ data.text }}</h5>
              <p class="text-white">{{ data.paratext }}</p>
            </div>
          </div>
        </div>
      </div>
      <div class="row justify-content-center">
        <div class="col-lg-6">
          <div class="text-center py-4">
            <ButtonOne text="View All Services "></ButtonOne>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="legacy">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6">
<div class="legacy_text">

  <h5 class="text-white">2017 - A Legacy of Innovation</h5>
  <p class="text-white">Early Years: In the early years, Steve Jobs recognized the growing importance of technology in
     business and set out to create a company that could help organizations leverage the power
      of digital innovation. With a small team of passionate individuals.</p>
      <p class="text-white">Expansion & Innovation: As technology continued to evolve,
         so did [Company Name]. We expanded our service offerings to include a wide range of solutions,
          from cybersecurity and cloud computing to data analytics and artificial intelligence.</p>
</div>
        </div>
        <div class="col-lg-6">
          <div class="lagacy_img">
            <img src="../assets/images/about-tab-img.png" alt="" class="img-fluid">
          </div>
        </div>
      </div>
    </div>
  </section>
  </template>
  <script>
  import MainTitle from '@/components/MainTitle.vue';
  import ButtonOne from '@/components/ButtonOne.vue';

  export default {
    name: 'HomeView',
    components: {
      MainTitle, ButtonOne
    },
    data() {
    return {
      data: [
        {
          path: "icon1.png",
          text: "Consulting Service",
          paratext: "Strategic IT planning roadmap development Business process analysis and improvement for It solution & technology.",
        },
        {
          path: "icon2.png",
          text: "Software Development",
          paratext: "Mobile app development for iOS, Android, and cross-platform solutions & web application.",
        },
        {
          path: "icon3.png",
          text: "Cloud Solution",
          paratext: "Infrastructure as a Service (IaaS), Platform as a Service (PaaS), and Software as a Service(SaaS)",
        },
        {
          path: "icon4.png",
          text: "Cyber Security",
          paratext: "Threat assessment and vulnerability analysis. Security strategy development and implementation",
        },
        {
          path: "icon5.png",
          text: "Data Analytics",
          paratext: "Threat assessment and vulnerability analysis. Security strategy development and implementation",
        },
        {
          path: "icon6.png",
          text: "Manage It Services",
          paratext: "Proactive IT monitoring and management Network infrastructure setup and maintenance",
        },
      ],
  
    };
  }
  }
  
  </script>
  
  <style scoped>
.our_services_detail {
  padding: 50px 0 100px 0;
}

.our_services_detail .card-b {
  background-color: var(--bg-1);
  padding: 35px 25px;
  border: 1px solid transparent;
  border-radius: 4px;
  transition: .5s ease-in-out;
}

.our_services_detail .card-b:hover {
  border: 1px solid var(--light-yellow);

}

.our_services_detail .card-b .icon-box {
  background-color: var(--main_black);
  border-radius: 50%;
  height: 60px;
  width: 60px;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 15px;
}
.legacy{
  padding-bottom: 100px;
}
@media only screen and (min-width: 320px) and (max-width: 991px){
  .legacy{
    text-align: center;
  }
}
</style>