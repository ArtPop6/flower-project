<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <swiper /> -->
    <Awesome />
  </div>
</template>


<script>
// @ is an alias to /src
import Swiper from '@/components/Swiper.vue'
import Awesome from '@/components/Awesome.vue'

export default {
  name: 'home',
  components: {
    Swiper,
    Awesome
  }
}
</script>
