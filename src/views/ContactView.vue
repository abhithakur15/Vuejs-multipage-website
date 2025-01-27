<template>
<section class="contact">
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-lg-6">
        <div class="text-center set-text">
          <MainTitle text="Contact Detail" text1="Information"></MainTitle>
        </div>

      </div>
    
    </div>
    <div class="row justify-content-center my-4">

        <div class="col-lg-5 text-center">
<div class="box-info my-3">
  <div class="icon">
    <i class="fa-solid fa-phone text-white"></i>
  </div>
  <div class="text-box">
    <h6 class="text-white">Contact Us</h6>
 <p><a href="tel:+4733378901" class="text-white">+47 333 78 901</a></p>
  </div>
</div>
      </div>
  
      <div class="col-lg-5 text-center">
<div class="box-info my-3">
  <div class="icon">
    <i class="fa-solid fa-envelope text-white"></i>
  </div>
  <div class="text-box">
    <h6 class="text-white">Send Us a Mail</h6>
 <p><a href="mailto:someone@example.com" class="text-white">Send email</a></p>
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
    }

  }
  
  </script>
  <style scoped>
  .contact{
    padding: 50px 0 100px 0;
  }
  .box-info {
    border: 1px solid var(--light-yellow);
    padding: 50px 0;
    text-align: center;
    border-radius: 4px;
    background-color: var(--bg-1);
}
.box-info .icon i{
font-size: 30px;
}
.box-info .icon{
  margin:10px;
}
.box-info  .text-box  h6{
font-size: 30px;
}
</style>
  