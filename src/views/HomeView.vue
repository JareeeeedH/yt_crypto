<template>
  <div class="home">
    <!-- 輪播 -->
    <Carousel />
    <!-- 買/賣盤價 -->
    <PriceTable />

    <main class="main-content">
      <div class="about-us">
        <div class="about-text">
          <img class="about-us-title" src="" alt="" />
          <div class="about-us-content">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Libero
            possimus molestiae perspiciatis, eaque culpa nam unde laboriosam
            quia doloremque minima.
          </div>
        </div>
        <div class="about-img">
          111
          <img src="" alt="" />
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import Carousel from "@/components/Carousel.vue";
import PriceTable from "@/components/PriceTable.vue";

export default {
  name: "HomeView",
  components: {
    Carousel,
    PriceTable,
  },
};
</script>

<style lang="scss">
.about-us {
  display: flex;
}
</style>
