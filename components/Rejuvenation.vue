<template>
  <section>
    <v-container>
      <h2>
        OCMD Rejuvenation <br>
        Complex Cream
      </h2>
      <div v-view class="rejuvenation_images">
        <img
          v-view="viewHandler"
          src="@/assets/images/vector_2.png"
          :class="{ active: inview }"
          alt=""
        >
        <img
          v-view="viewHandler"
          src="@/assets/images/vector_1.png"
          :class="{ active: inview }"
          alt=""
        >
        <img
          v-view="viewHandler"
          src="@/assets/images/cream.png"
          :class="{ active: inview }"
          alt=""
        >
      </div>
      <DHL />
      <div v-view class="product-list">
        <div class="product-list_item">
          <img src="@/assets/images/cream.png" alt="">
          <div class="product-list_item_name">
            <b>
              2-Weeks Challenge <br>
              Sample Kit</b>
          </div>
          <div class="product-list_item_vol">
            Volume: 20ml / 0.67oz
          </div>
          <div class="product-list_item_price">
            Only $22.95
          </div>
          <div class="product-list_item_order-now">
            ORDER NOW
          </div>
          <div class="product-list_item_or">
            OR
          </div>
          <img src="@/assets/images/paypal.png" alt="" srcset="">
        </div>
        <div class="product-list_item">
          <img src="@/assets/images/cream.png" alt="">
          <div class="product-list_item_name">
            <b> OCMD Rejuvenation <br> Complex Cream (Full Size)</b>
          </div>
          <div class="product-list_item_vol">
            Volume: 60ml / 2.03oz
          </div>
          <div class="product-list_item_price">
            <div class="old-price">
              $69
            </div>  $49
          </div>
          <div class="product-list_item_order-now">
            ORDER NOW
          </div>
          <div class="product-list_item_or">
            OR
          </div>
          <img src="@/assets/images/paypal.png" alt="" srcset="">
        </div>
        <div class="product-list_item">
          <img src="@/assets/images/cream-group.png" alt="">
          <div class="limited">
            Limited edition
          </div>
          <div class="product-list_item_name">
            <b>
              60ml OCMD Rejuvenation Complex
              Cream - 2 Pack
            </b>
          </div>
          <div class="product-list_item_vol">
            Volume: 60ml / 2.03oz Each
          </div>
          <div class="product-list_item_price">
            <div class="old-price">
              $138
            </div>  $88
          </div>
          <div class="product-list_item_order-now">
            ORDER NOW
          </div>
          <div class="product-list_item_or">
            OR
          </div>
          <img src="@/assets/images/paypal.png" alt="" srcset="">
        </div>
      </div>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'RejuvenationComponent',
  data () {
    return {
      inview: false
    }
  },
  methods: {
    viewHandler (e) {
      if (e.type === 'enter') {
        this.inview = true
      }
    }
  }
}
</script>

<style scoped>

section {
  margin-top: 40px;
}
.limited {
  transform: rotate(45deg) translate(33%, -200%);
  background: #23a455;
  top: 0;
  left: 0;
  width: 100%;
  height: 20px;
  position: absolute;
  color: #fff;
  text-align: center;
}
h2 {
  font-family: "Roboto";
  font-weight: bold;
  text-align: center;
  color: #0075b2;
  font-size: 40px;
}

.old-price{
  text-decoration: line-through;
  display: inline-block;
}

.rejuvenation_images {
  height: 450px;
  margin: 0 auto;
  position: relative;
  display: flex;
  justify-content: center;
  text-align: center;
  align-items: flex-end;
}

.rejuvenation_images img {
  max-width: 100%;
  max-height: 100%;
  position: absolute;
  transition: 0.5s;
  opacity: 0;
  top: 100%;
}

.rejuvenation_images img.active {
  top: auto;
  opacity: 1;
}

.product-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;

}

.product-list_item {
  flex:0 1 calc(33% - 1em);
  overflow: hidden;
  font-family: "Roboto";
  padding: 38px;
  background: #fff;
  border-radius: 20px;
  filter: drop-shadow(0 0 2px rgba(0, 0, 0, 0.09));
  text-align: center;
   margin-top: 60px;
}
.product-list_item img {
  width: 100%;
  max-width: 250px;
}
.product-list_item_name {
  margin-top: 40px;
  font-size: 20px;
}
.product-list_item_vol {
  font-size: 20px;
  margin-top: 23px;
}
.product-list_item_price {
  color: #46ae46;
  font-weight: bold;
  font-size: 30px;
  margin-top: 23px;
}
.product-list_item_order-now {
  color: #fff;
  background: #46ae46;
  font-weight: bold;
  font-size: 20px;
  border-radius: 10px;
  padding: 10px 0;
  margin-top: 23px;
  transition: 0.3s;
  cursor: pointer;
}

.product-list_item_order-now:hover {
  transform: scale(1.3);
}
.product-list_item_or {
  margin: 23px 0;
  font-size: 22px;
}

@media (max-width: 990px) {
  .product-list_item {
    margin-top: 60px;
    flex: 0 1 100%;
  }

  .limited {
    transform: rotate(45deg) translate(33%, -400%);
  }
}
@media (max-width: 576px) {
  .limited {
    transform: rotate(45deg) translate(33%, -200%);
  }
  h2 {
    font-size: 30px;
  }
}
</style>
