<template>

  <!-- 之後價格有要從上層丟資料進來，再寫props接資料 -->
  <!-- 盤價 -->
  <div class="price-table">

    <!-- Usdt icon -->
    <div class="usdt-col">
      <img src="../assets/USDT.png" alt="usdt-logo" class="usdt-logo">
      &nbsp;
      <span>USDT</span>
    </div>

    <!-- price -->
    <div class="price-col">
      <div class="buy-col">
        <span class="buy-icon">買</span>
        &nbsp;
        <span>30.111 TWD</span>
      </div>
      <div class="sell-col">
        <span class="sell-icon">賣</span>
        &nbsp;
        <span>30.111 TWD</span>
      </div>
    </div>

    <!-- button -->
    <div class="button-col">
      <button class="exchange-btn">立即交易</button>
    </div>

  </div>
</template>

<script>

export default {
  name: 'PriceTable',
}
</script>


<style lang="scss">

@mixin inCenter {
  display: flex;
  justify-content: center;
  align-items: center;
}

.price-table{
  display: flex;
  position: relative;
  width: 55%;
  height: 100px;
  margin-top: 20px;
  border: 1px solid black;
  border-radius: 5px;
  left: 50%;
  transform: translateX(-50%);

  div{
    flex:1;
  }
}

.usdt-logo{
  width: 25px;
}


.usdt-col{
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: .85rem;
}

.price-col{
  @include inCenter();
  flex-direction: column;

  .buy-col, .sell-col{
    @include inCenter();
  }
}

.button-col{
  @include inCenter();
}

.exchange-btn{
    width: 110px;
    padding: 5px;
    border-radius: 200px;
    border: none;
    font-size: 1rem;
    font-weight: bold;
    color: white;
    cursor: pointer;
    background: linear-gradient(to left, #3DA1E6, #61CDAE);
}

.buy-icon, .sell-icon{
  width: 20px;
  height: 20px;
  text-align: center;
  color: rgb(250, 250, 250);
  font-size: .25rem;
  line-height:20px;
  border-radius: 2px;
}

.sell-icon{
  background-color: #00B900;
}

.buy-icon {
  background-color: #FA5151;
}



@media screen and (max-width: 768px) {

  .price-table{
    width: 90%;
  }

}
</style>