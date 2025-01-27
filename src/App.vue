<template>
<HeaderFile></HeaderFile>
  <!-- <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav> -->
  <router-view/>
  <FooterFile></FooterFile>
</template>



<script>
import HeaderFile from './components/HeaderFile.vue';
import FooterFile from './components/FooterFile.vue';
export default {
  name: "app",
  components: {
   HeaderFile,
   FooterFile

  }
}



</script>
<style>
:root {
  --white: #ffffff;
--light-yellow:#A1E934;
--black:#0D0E10;
--bg-1:#1E182D;
--main_black:#000000;
}
body{
  background-image: url('../src/assets/images/body2.png');
  font-family: "Figtree", serif !important;
  background-position: center center;
    background-repeat: no-repeat;
    background-size: cover;
}
a{
  text-decoration: none !important;
}
.our_services_detail .set-text .main-title .d-flex.align-items-center.gap-2.mb-3,
.team .set-text .main-title .d-flex.align-items-center.gap-2.mb-3,
.contact  .set-text .main-title .d-flex.align-items-center.gap-2.mb-3{
  justify-content: center !important;
}

/* for sticky  css start*/
.sticky {
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 9;
    background-color: #000030;
  }
  /* for sticky  css end*/

  
/**************************************************** animation header css start **********************************************/

.animated {
    -webkit-animation-duration: 1s;
    animation-duration: 1s;
    -webkit-animation-fill-mode: both;
    animation-fill-mode: both;
  }
  
  .fadeInDown {
    -webkit-animation-name: fadeInDown;
    animation-name: fadeInDown
  }
  
  @-webkit-keyframes fadeInDown {
    0% {
      opacity: 0;
      -webkit-transform: translate3d(0, -100%, 0);
      transform: translate3d(0, -100%, 0)
    }
  
    to {
      opacity: 1;
      -webkit-transform: none;
      transform: none
    }
  }
  
  @keyframes fadeInDown {
    0% {
      opacity: 0;
      -webkit-transform: translate3d(0, -100%, 0);
      transform: translate3d(0, -100%, 0)
    }
  
    to {
      opacity: 1;
      -webkit-transform: none;
      transform: none
    }
  }
  /**************************************************** animation header css end **********************************************/

  

/* **************************toggle cross in menu bar ********************************************/

.navbar-toggler {
    border: 0 !important;
  }
  
  .navbar-toggler:focus,
  .navbar-toggler:active,
  .navbar-toggler-icon:focus {
    outline: none !important;
    box-shadow: none !important;
    border: 0 !important;
  }
  
  /* Lines of the Toggler */
  .toggler-icon{
    width: 30px;
    height: 3px;
    background-color: var(--light-yellow);
    display: block;
    transition: all 0.2s;
  }
  
  /* Adds Space between the lines */
  .middle-bar{
    margin: 5px auto;
  }
  
  /* State when navbar is opened (START) */
  
  .navbar-toggler[aria-expanded="true"] .top-bar {
    transform: rotate(45deg);
    transform-origin: 10% 10%;
  }
  
  .navbar-toggler[aria-expanded="true"] .middle-bar {
    opacity: 0;
    filter: alpha(opacity=0);
  }
  
  .navbar-toggler[aria-expanded="true"] .bottom-bar {
    transform: rotate(-45deg);
    transform-origin: 10% 90%;
  }
  /* State when navbar is opened (END) */
  
  /* State when navbar is collapsed (START) */
  .navbar-toggler.collapsed .top-bar {
    transform: rotate(0);
  }
  
  .navbar-toggler.collapsed .middle-bar {
    opacity: 1;
    filter: alpha(opacity=100);
  }
  
  .navbar-toggler.collapsed .bottom-bar {
    transform: rotate(0);
  }
  /* State when navbar is collapsed (END) */
  
  /* Color of Toggler when collapsed */
  .navbar-toggler.collapsed .toggler-icon {
    background-color: var(--light-yellow);
  }
  /* **************************toggle cross in menu bar end********************************************/

/* responsive css */

@media only screen and (min-width: 320px) and (max-width: 575px){
  .hero .hero-text h1,    .main-title h2 {
    font-size: 25px !important;
  
}
.our-services-image .about-1,
.our-services-image .about-2{
  display:none;
    }
    .demo-card {

    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.demo-card .icon {

    width: 75px !important;

}
.footer-logo {
    text-align: center;
    margin-bottom: 13px;
}

.hero {
    padding: 55px 0;
}
.hero-image {
    margin-bottom: 10px;
}
.team-a {
    text-align: center;
}
.main-title span[data-v-4dd5a89f] {

    justify-content: center;
}

}

@media only screen and (min-width: 576px) and (max-width: 767px){
  .hero .hero-text span{

    justify-content: center;
}
.hero .hero-text h1 {
    font-size: 35px !important;
text-align: center;
}
.our-services-image .about-1,
.our-services-image .about-2{
  display:none;
    }
    .main-title span {

    margin-top: 25px;
    display: inline-block !important;
}
.main-title h2 {
    font-size: 35px !important;

}
.footer-logo {
    text-align: center;
    margin-bottom: 13px;
}
}

@media only screen and (min-width: 768px) and (max-width: 991px){
  .hero .hero-text h1 {
    font-size: 45px !important;

}
.our-services-image .about-1,
.our-services-image .about-2{
  display:none;
    }
    .our-services-image {
    text-align: center;
    margin-bottom: 30px;
}

.main-title span {
    justify-content: center;
}
.demo-card .icon {

    width: 100px;

}
.team-box {
    text-align: center;
}
}

@media only screen and (min-width: 320px) and (max-width: 1400px){
  body,html{
  overflow-x: hidden;
}
}




</style>
