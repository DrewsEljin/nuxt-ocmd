<template>
  <section v-view>
    <div class="sale">
      <div class="old-price">
        Only
        <div class="line-through">
          $44
        </div>
      </div>
      <div class="new-price">
        $22.95
      </div>
    </div>
    <div class="business-title">
      <div class="business-title_blue">
        FAST
      </div>
      2-4 Business Day
      <div class="business-title_blue">
        Shipping
      </div>
      in USA <br>
      From Our US Warehouses
    </div>
    <img class="dhl" src="@/assets/images/dhl.png" alt="">
    <div class="order-now">
      <div class="order-now_label">
        <div class="order-now_title">
          Order Yours Now
        </div>
        <div class="order-now_text">
          QUICK 2-4 Business Days Shipping
        </div>
      </div>
      <img src="@/assets/images/arrow.png" alt="">
    </div>
  </section>
</template>

<script>
export default {
  name: 'DhlComponent'
}
</script>

<style scoped>
.sale {
  white-space: nowrap;
  margin-top: 20px;
  text-align: center;
  font-family: "Roboto";
  display: flex;
  font-size: 40px;
  justify-content: center;
  align-items: center;
}

.sale .old-price {
  margin-right: 20px;
}
.sale .old-price .line-through {
  display: inline;
  text-decoration: line-through;
}
.sale .new-price {
  font-weight: bold;
}
.business-title {
  color: #727272;
  text-align: center;
  margin-top: 40px;
  font-family: "Roboto";
  font-size: 30px;
}
.business-title_blue {
  color: #0075b2;
  display: inline-block;
}
.dhl {
  display: block;
  margin: 30px auto 0 auto;
}
.order-now {
  margin: 40px auto 0 auto;
  background: #23a455;
  font-family: "Roboto";
  padding: 20px 30px;
  max-height: 85px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-radius: 20px;
  color: #fff;
  max-width: 400px;
  transition: 0.3s;
  cursor: pointer;
}
.order-now:hover{
  transform: scale(1.3);
}

.order-now_label {
  text-align: center;
}
.order-now_title {
  font-size: 25px;
}
.order-now_text {
  font-size: 18px;
  color: rgba(186, 224, 197, 1);
}
</style>
