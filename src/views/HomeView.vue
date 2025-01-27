<template>
  <section class="hero">
    <div class="container">
      <div class="row align-items-center flex-column-reverse flex-md-row flex-lg-row">
        <div class="col-lg-6 col-md-6">
          <div class="hero-text">
            <span class="d-flex align-items-center gap-2 mb-3"><img src="../assets/images/span2.png" alt=""
                class="img-fluid"> TechXen Technology & It Solution</span>
            <h1 class="text-white">Empowering Your
              Digital Journey
              With TechXen</h1>
          </div>
        </div>
        <div class="col-lg-6 col-md-6">
          <div class="hero-image text-center">
            <img src="../assets/images/hero.png" alt="" class="img-fluid">
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="our-service">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6">
          <div class="our-services-image">
            <img src="../assets/images/about1.png" alt="" class="img-fluid">
            <img src="../assets/images/about2-img1.png" alt="" class="img-fluid about-1">
            <img src="../assets/images/about2-img3.png" alt="" class="img-fluid about-2">
          </div>
        </div>
        <div class="col-lg-6">
          <div class="our-service-text">
            <MainTitle text="Our Service" text1="Empower Your Business
With Our Comprehensive
IT Solutions"></MainTitle>
            <p class="text-white mb-4">Welcome to TechXen, your premier destination for cutting-edge technology
              solutions and IT services.
              At TechXen, we are passionate about harnessing the power of technology to empower businesses a like.</p>
            <div class="card-a">
              <div class="progres-line-1 mb-4">
                <h6 class="text-white mb-3">IT Consulting</h6>
                <div class="progress" role="progressbar" aria-label="Basic example" aria-valuenow="100"
                  aria-valuemin="0" aria-valuemax="100">
                  <div class="progress-bar" style="width: 100%"></div>
                </div>
              </div>
              <div class="progres-line-1">
                <h6 class="text-white mb-3">Cyber Security</h6>
                <div class="progress" role="progressbar" aria-label="Basic example" aria-valuenow="75" aria-valuemin="0"
                  aria-valuemax="75">
                  <div class="progress-bar" style="width: 75%"></div>
                </div>
              </div>
            </div>
            <div class="button-b">
              <ButtonOne text="Learn More "></ButtonOne>
            </div>

          </div>
        </div>
      </div>
    </div>
  </section>

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
        <div class="col-lg-4 col-md-6 col-sm-6 my-3 " v-for="(data, index) in data" :key="index">
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

<section class="base_it ">
  <div class="container">
    <div class="row justify-content-between flex-column-reverse flex-lg-row">
      <div class="col-lg-5">
        <div class="base-it-text">
          <MainTitle text="Best It Solution" text1="Let's Elevate Your Business
With Strategic IT Solutions"></MainTitle>
<p class="text-white">At TechXen, we understand that every business is unique, which is why we offer a range of flexible 
  IT solutions designed to address your specific challenges and goals.</p>
  <DemoCard text="Network Infrastructure Solutions" text1="Build a reliable and secure network infrastructure that
supports your business operations enables seamless" path="solution-iocn1"></DemoCard>
<div class="mt-3">
  <DemoCard text="Managed It Services" text1="Focus on your core business activities while we take
care of your IT needs with our managed IT services." path="solution-iocn2"></DemoCard>
</div>
        </div>
      </div>
      <div class="col-lg-6">
        <div class="our-services-image">
            <img src="../assets/images/about1.png" alt="" class="img-fluid">
            <img src="../assets/images/about2-img1.png" alt="" class="img-fluid about-1">
            <img src="../assets/images/about2-img3.png" alt="" class="img-fluid about-2">
          </div>
      </div>
    </div>
  </div>
</section>

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
      <div class="col-lg-3 col-sm-6 mb-2" v-for="(data, index) in data1" :key="index">
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
import ButtonOne from '@/components/ButtonOne.vue';
import DemoCard from '@/components/DemoCard.vue';
export default {
  name: 'HomeView',
  components: {
    MainTitle, ButtonOne,DemoCard
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
    }
  ]
  };
}
}

</script>
<style scoped>
.hero {
  padding: 100px 0;
}

.hero .hero-text span {
  color: var(--light-yellow);
  font-size: 16px;
  font-weight: 700;
}

.hero .hero-text h1 {
  font-size: 64px;
  font-weight: 700;
}

.hero .hero-image img {
  animation-name: shape-animaiton4;
  animation-duration: 82s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
  animation-timing-function: ease-in-out;
}

@keyframes shape-animaiton4 {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(1000deg);
  }
}

.card-a .progres-line-1 h6 {
  font-size: 20px;
  font-weight: 700;
}

.progress-bar {
  background-color: var(--light-yellow);
}

.card-a {
  background-color: var(--bg-1);
  padding: 30px 40px;
  border-radius: 10px;
}

.our-service {
  padding-bottom: 100px;
}

.our-services-image {
  position: relative;
}

.our-services-image .about-1 {
  position: absolute;
  top: 0;
  z-index: 3;
  left: -17%;
}

.our-services-image .about-2 {
  position: absolute;
  bottom: -20%;
  z-index: 3;
  right: 4%;
}

.our-service .button-b {
  margin-top: 47px;
}

.our_services_detail {
  padding-bottom: 100px;
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
.team{
  padding: 100px 0;
}
</style>