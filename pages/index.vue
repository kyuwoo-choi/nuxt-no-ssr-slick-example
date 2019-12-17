<template>
  <div class="carousel-wrapper">
    <no-ssr>
      <slick :options="slickOptions">
        <div v-for="i in 5" :key="i" class="img-warpper">
          <img :src="`https://picsum.photos/200/100?random=${i}`" />
        </div>
      </slick>
    </no-ssr>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slickOptions: {
        slidesToShow: 3
      }
    }
  }
}
</script>

<style>
.carousel-wrapper {
  padding: 40px;
}
.img-warpper img {
  margin: auto;
  width: 200px;
  height: 100px;
  background-image: linear-gradient(gray 100%, transparent 0);
}
.slick-next:before, .slick-prev:before {
  color: black;
}
</style>
