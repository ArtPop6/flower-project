<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <swiper /> -->
    <Carousel />
  </div>
</template>


<script>
// @ is an alias to /src
// import Swiper from "@/components/Swiper.vue";
import Carousel from "../components/Carousel.vue";

export default {
  name: "home",
  components: {
    Carousel
  }
};
</script>
