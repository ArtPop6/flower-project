<template>
  <div class="block">
    <el-carousel height="150px">
      <el-carousel-item v-for="item in imgs" :key="item">
        <img :src="item.src" alt="">
      </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script>
export default {
    name: 'Carousel',
    data() {
        return {
            imgs: [
                {
                    src: require('../assets/haidi.png')
                },
                {
                    src: require('../assets/tasha.png')
                },
                {
                    src: require('../assets/yuzhuan.png')
                },
                {
                    src: require('../assets/zhuiyue.png')
                }
            ]
        }
    },
}
</script>

<style>
  .el-carousel__item img {
    width: 100%;
    height: 100%;
    margin: 0;
  }
</style>