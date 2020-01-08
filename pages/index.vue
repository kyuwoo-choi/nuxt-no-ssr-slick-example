<template>
  <div class="carousel-wrapper">
    <client-only>
      <slick :options="slickOptions">
        <div v-for="i in 5" :key="i" class="img-wrapper">
          <img :src="`./${i}-200x100.jpg`" />
        </div>
      </slick>
    </client-only>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slickOptions: {
        arows: false,
        dots: true,
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
.img-wrapper img {
  margin: auto;
  width: 200px;
  height: 100px;
  background-image: linear-gradient(gray 100%, transparent 0);
}
</style>
