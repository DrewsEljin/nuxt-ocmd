<template>
  <section v-view>
    <v-container>
      <h2><i>Real Customers</i> Results</h2>
      <div class="slider-result">
        <vue-tiny-slider v-bind="tinySliderOptions">
          <div>
            <div class="slider_item">
              <div class="cell">
                <img src="@/assets/images/slider1_1.png" alt="">
              </div>
              <div class="cell">
                <img src="@/assets/images/slider1_2.png" alt="">
              </div>
              <div class="slider_circle">
                <p>Julia</p>
                <p>United States,</p>
                <p>Age: 43</p>
              </div>
            </div>
          </div>
          <div>
            <div class="slider_item">
              <div class="cell">
                <img src="@/assets/images/slider2_1.png" alt="">
              </div>
              <div class="cell">
                <img src="@/assets/images/slider2_2.png" alt="">
              </div>
              <div class="slider_circle">
                <p>Aliza</p>
                <p>United States,</p>
                <p>Age: 70</p>
              </div>
            </div>
          </div>
          <div>
            <div class="slider_item">
              <div class="cell">
                <img src="@/assets/images/slider3_1.png" alt="">
              </div>
              <div class="cell">
                <img src="@/assets/images/slider3_2.png" alt="">
              </div>
              <div class="slider_circle">
                <p>Afsaneh</p>
                <p>France,</p>
                <p>Age: 55</p>
              </div>
            </div>
          </div>
          <div>
            <div class="slider_item">
              <div class="cell">
                <img src="@/assets/images/slider4_1.png" alt="">
              </div>
              <div class="cell">
                <img src="@/assets/images/slider4_2.png" alt="">
              </div>
              <div class="slider_circle">
                <p>Alison</p>
                <p>United Kingdom,</p>
                <p>Age: 57</p>
              </div>
            </div>
          </div>
          <div>
            <div class="slider_item">
              <div class="cell">
                <img src="@/assets/images/slider5_1.png" alt="">
              </div>
              <div class="cell">
                <img src="@/assets/images/slider5_2.png" alt="">
              </div>
              <div class="slider_circle">
                <p>Gabriella</p>
                <p>United States,</p>
                <p>Age: 65</p>
              </div>
            </div>
          </div>
        </vue-tiny-slider>
      </div>
      <div>
        <ul class="advantages-list">
          <li>
            <span><b> Helps Reducing the appearance of wrinkles.</b></span>
          </li>
          <li>
            <span>Helps Firming and lifting the skin (for over 92% of
              customers)</span>
          </li>
          <li>
            <span>Removes Dead Surface Skin Cells to Help Creating a brighter
              complexion.</span>
          </li>
          <li>
            <span>
              Swiss Apple Stem Cells Helps stimulate skin stem cell regeneration
              by up to 80%.</span>
          </li>
          <li>
            <span>
              Helps reducing the damage of UV sun light on skin stem cells by
              46%.</span>
          </li>
        </ul>
      </div>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'ResultComponent',

  data () {
    return {
      tinySliderOptions: {
        mouseDrag: true,
        loop: true,
        items: 1,
        swipeAngle: 45,
        nav: true,
        navPosition: 'bottom',
        nonce: true
      }
    }
  },
  head: {
    link: [
      {
        rel: 'stylesheet',
        href: 'https://cdnjs.cloudflare.com/ajax/libs/tiny-slider/2.9.1/tiny-slider.css'
      }
    ]
  }
}
</script>

<style scoped>
h2 {
  text-align: center;
  font-size: 30px;
  font-family: "PlayfairDisplay";
  margin-bottom: 40px;
}

h2 i {
  color: #bf8876;
}

ul.advantages-list {
  text-align: center;
  list-style-image: url("@/assets/images/success.png");
  display: flex;
  margin: 0 auto;
  flex-direction: column;
  max-width: 450px;
  font-family: "Roboto";
  color: #54595f;
  font-size: 20px;
  margin-top: 40px;
  line-height: 30px;
}

ul.advantages-list li {
  width: 100%;
  text-align: left;
}

ul.advantages-list li span {
  position: relative;
  left: 20px;
}

/* ul.advantages-list li::before{
content:'';
width: 16px;
height: 14px;
display: inline-block;
background-size: contain;
margin-right: 23px;
} */
.slider-result {
  padding-bottom: 50px;
}
.slider_circle {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 18px;
  background: #fff;
  font-weight: bold;
  font-family: "Roboto";
  display: flex;
  justify-content: center;
  flex-direction: column;
  height: 150px;
  width: 150px;
  border-radius: 100px;
}
.slider_item {
  position: relative;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 20px;
}
.slider_item img {
  max-width: 100%;
}

@media (max-width: 768px) {
  .advantages-list {
    padding: 0 30px;
  }
}
@media (max-width: 576px) {
  .slider_circle {
    transform: translate(-50%, -50%) scale(0.65);
  }
}
</style>
