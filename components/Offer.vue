<template>
  <section v-view>
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/tiny-slider/2.9.1/tiny-slider.css"
    >
    <div class="limited">
      Limited Offer!!!!
    </div>
    <v-container>
      <h2>
        Claim Your Limited Edition <br>
        Starter-Kit While Supply Last...
      </h2>
      <DHL />
      <div class="stem-cells">
        Proudly introducing the revolutionary <br>
        technology of <b>Apple Stem Cells</b> <br>
        that helps <b> <i> firming </i></b> and <b> <i> lifting </i></b>skin…
        <br>
        while reducing the appearance of wrinkles depth!
      </div>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'OfferComponent'
}
</script>

<style scoped>

h2 {
  margin-top: 40px;
  color: #0075b2;
  font-family: "Roboto";
  font-weight: bold;
  font-size: 40px;
  text-align: center;
}
.limited {
  width: 100%;
  background: #000;
  color: #fff;
  font-size: 46px;
  font-weight: bold;
  padding: 25px 0;
  text-align: center;
  font-family: "PlayfairDisplay";
}

.stem-cells {
  margin-top: 40px;
  font-family: "Roboto";
  font-size: 30px;
  line-height: 48px;
  text-align: center;
  color: #54595f;
}
</style>
