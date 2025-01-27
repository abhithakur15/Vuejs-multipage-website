<template>
  <section class="our-service pt-5">
    <div class="container">
      <div class="row align-items-center flex-column-reverse flex-lg-row">
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
              <ButtonOne text="Learn More " path="javascript:void(0)"></ButtonOne>
            </div>

          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="base_it">
  <div class="container">
    <div class="row justify-content-between align-items-center flex-column-reverse flex-lg-row">
      <div class="col-lg-5">
        <div class="base-it-text">
          <MainTitle text="Best It Solution" text1="Let's Elevate Your Business
With Strategic IT Solutions"></MainTitle>
<p class="text-white">At TechXen, we understand that every business is unique, which is why we offer a range of flexible 
  IT solutions designed to address your specific challenges and goals.</p>

<p class="text-white">At TechXen, our mission is simple: to revolutionize the digital landscape by delivering top-notch technology solutions that drive growth, efficiency, and sustainability for our clients. We strive to be the trusted partner that businesses can rely on to navigate the complexities of the digital world.</p>
<p class="text-white">"At TechXen, our mission is to empower businesses through technology. We believe in harnessing the power of innovation to drive growth, efficiency, and sustainability for our clients. Through our tailored technology solutions and unwavering commitment to excellence, we strive to be the catalyst for positive change in the digital landscape.</p>       
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
</template>

<script>
import MainTitle from '@/components/MainTitle.vue';
import ButtonOne from '@/components/ButtonOne.vue';

export default {
  name: 'HomeView',
  components: {
    MainTitle, ButtonOne
  }

}



</script>
<style scoped>
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

.base_it{
  padding: 100px 0;
}
@media only screen and (min-width: 320px) and (max-width: 991px){
  .our-service{
text-align: center;
  }
  .our-services-image{

    margin-top: 60px;
}
.base_it{
  text-align: center;
}
.base_it {
    padding: 0 0 100px 0;
}
.base_it .our-services-image{
  margin-top: 0px;
  margin-bottom: 60px;
}
}
</style>
