<template>
  <!-- :autoplay="{ autoplay: true }" -->
  <div class="swiper-container">
    <swiper
      :pagination="{
        dynamicBullets: true,
      }"
      :navigation="true"
      :modules="modules"
      class="mySwiper"
    >
      <swiper-slide v-for="banner in bannerInfo">
        <img :src="banner.imgSrc" />
        <div class="banner-info">
          <h2 class="banner-title">{{ banner.bannerTitle }}</h2>
          <h5 class="banner-subTitle">{{ banner.bannerSubTitle }}</h5>
          <button class="banner-btn">{{ banner.btnText }}</button>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// import styles
import "swiper/css";
import "swiper/css/pagination";
import "swiper/css/navigation";

// import All, 如果覺得麻煩
// import 'swiper/css/bundle'

// import required modules
import { Navigation, Pagination, Autoplay } from "swiper";

//
import { onMounted } from "vue";

export default {
  name: "carousel",
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    // Banner資料
    const bannerInfo = [
      {
        imgSrc: require("../assets/banner/banner01.png"),
        bannerTitle: "最速交易平台",
        bannerSubTitle: "買/賣 手續費 0.00%",
        btnText: "開始交易",
      },
      {
        imgSrc: require("../assets/banner/banner02.png"),
        bannerTitle: "搶先註冊會員",
        bannerSubTitle: "就享瓜分 5000 USDT 獎勵資格！",
        btnText: "立即註冊",
      },
      {
        imgSrc: require("../assets/banner/banner03.png"),
        bannerTitle: "無腦賺息",
        bannerSubTitle: "年化利率 12% 業界最優",
        btnText: "立即鎖幣",
      },
      {
        imgSrc: require("../assets/banner/banner04.png"),
        bannerTitle: "等待確認Title",
        bannerSubTitle: "待確認 suvTitle",
        btnText: "高雄發大財",
      },
    ];

    onMounted(() => {
      console.log("mounted !");
    });

    return {
      modules: [Navigation, Pagination, Autoplay],
      bannerInfo,
    };
  },
};
</script>

<style lang="scss" scoped>
.swiper-container {
  width: 100%;
}
.mySwiper {
  position: relative;
  width: 100%;
}

.swiper-slide img {
  width: 100%;
}

.banner-info {
  position: absolute;
  left: 10%;
  top: 30%;
}

.banner-title {
  font-size: 2.5rem;
}

.banner-subTitle {
  font-size: 1.25rem;
}

.banner-btn {
  margin-top: 20px;
  width: 200px;
  padding: 10px;
  border-radius: 200px;
  border: none;
  font-size: 1rem;
  font-weight: bold;
  color: white;
  cursor: pointer;
  background: linear-gradient(to left, #3da1e6, #61cdae);
}

.banner-btn:hover {
  background: transparent;
  color: #3da1e6;
  border: 2px solid #3da1e6;
}

@media screen and (max-width: 768px) {
  .swiper-slide img {
    height: 45vh;
  }

  .banner-title {
    font-size: 1.25rem;
  }

  .banner-subTitle {
    font-size: 1.25rem;
  }
}
</style>
