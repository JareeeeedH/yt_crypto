<template>
  <div class="home">
    <!-- 輪播 -->
    <Carousel />
    <!-- 買/賣盤價 -->
    <PriceTable />

    <main class="main-content">
      <!-- about us -->
      <div class="about-us">
        <!-- left -->
        <div class="about-text">
          <img class="about-us-title" src="@/assets/text/about-us.png" />
          <br />
          <br />
          <p>
            YT
            Crypto平台不同於常見的撮合式交易平台，我們提供更簡便、更安全、更快速的服務讓您的資產與虛擬資產間的流通暢行無阻。
            <br />
            <br />
            「Not your key, Not your
            coin」是幣圈廣為流傳的一句名言，我們做到了真正的去中心化，讓您的虛擬資產「in
            your key」，這也是虛擬貨幣真正的核心價值，也是YT
            Crypto平台的核心價值。
            <br />
            <br />
            YT是經由主關機關核准設立，並做好AML/CFT工作，更有強大的資安系統支持，讓您更安心地與我們建立關係。
          </p>
        </div>
        <!-- right -->
        <div class="about-img">
          <img src="@/assets/about-img.png" />
        </div>
      </div>
      <!-- register button -->
      <button class="register-button">立即註冊</button>
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
.main-content {
  padding: 0 150px;
}

.about-us {
  padding: 80px 0;
  display: flex;

  font-size: 1.05rem;
  color: rgba(0, 0, 0, 0.55);
}

.about-text {
  width: 50%;
}

.about-img {
  width: 50%;
}

.about-us-title {
  width: 150px;
}

.about-img {
  display: flex;
  justify-content: center;
  align-items: center;
  // text-align: right;
  img {
    width: 60%;
  }
}

.register-button {
  display: none;
  position: relative;
  margin-top: 30px;
  width: 350px;
  padding: 10px;
  left: 50%;
  transform: translateX(-50%);
  border-radius: 200px;
  border: none;
  font-size: 1rem;
  font-weight: bold;
  color: white;
  cursor: pointer;
  background: linear-gradient(to left, #3da1e6, #61cdae);
}

@media screen and (max-width: 768px) {
  .main-content {
    padding: 50px;
  }

  .about-us {
    display: flex;
    align-items: center;
    flex-direction: column;
    padding: 0;
  }

  .about-text,
  .about-img {
    width: 100%;
  }

  .register-button {
    display: block;
  }
}
</style>
