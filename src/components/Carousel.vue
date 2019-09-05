<template>
  <div class="block">
    <el-carousel height="150px">
      <el-carousel-item v-for="item in carouselArr" :key="item">
        <img :src="item.url" />
      </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script>
export default {
  name: "Carousel",
  data() {
    return {
      autoplay: true,
      carouselArr: [
        { url: require("../assets/haidi.png") },
        { url: require("../assets/timg.jpg") },
        { url: require("../assets/tasha.png") }
      ]
    };
  }
};
</script>

<style>
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}

.el-carousel__item {
  width: 100%;
  height: 100px;
  background-color: grey;
}

img {
  width: 95%;
}
</style>