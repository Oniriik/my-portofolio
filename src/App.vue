<template>
  <div class="page-wrapper">
    <div class="home bloc">
      <!-- <AppNavbar/> -->
      <MyProfile/>
    </div>
    <div class="infos">
      <DisplayInfos/>
    </div>
    <div class="contact-bloc">
      <DisplayContact/>
    </div>
  </div>
  
  
</template>

<script>
// import AppNavbar from "./components/AppNavbar.vue"
import MyProfile from "./components/MyProfile.vue"
import DisplayInfos from './components/DisplayInfos.vue'
import DisplayContact from './components/DisplayContact.vue'

export default {
  name: 'App',
  components: {
    // AppNavbar,
    MyProfile,
    DisplayInfos,
    DisplayContact
  },
}
</script>

<style>
@import "@/assets/style/style.css";

.page-wrapper{
  height: 100vh;
  overflow-y: scroll;
  scroll-snap-type: y proximity;
  scroll-behavior: smooth;
}
.bloc,.infos{
  scroll-snap-align: start;
  padding: 1em;
}
.infos{
  height: auto;
}
.home{
  background-image: url('@/assets/img/color2.png');
  background-repeat: no-repeat;
  background-position-x: right;
  background-position-y: top;
  background-size:60vw;
  height: 100vh;
}

@media (max-width: 1000px) {

    .container {
        width: 100%;
        max-width: 720px;
        margin: 0 auto;
        padding: 0 2rem;
    }
    .home{
      background-size: 70vh;
    }
    .infos{
      height: auto;
    }
  }

  
body {
    animation: fadeInAnimation ease 3s;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
    overflow-y: hidden;
}
  
@keyframes fadeInAnimation {
    0% {
        opacity: 0;
    }
    100% {
        opacity: 1;
     }
}
</style>
