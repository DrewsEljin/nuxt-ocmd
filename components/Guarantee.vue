<template>
  <section v-view class="guarantee-section">
    <v-container>
      <img src="@/assets/images/duality.png" alt="">
      <div class="guarantee-section_text">
        <p>We are proud about our product and Stand Behind Our Promise!</p> <br> <br>

        Use the OCMD Rejuvenation Complex Cream Morning & Evening,<br>
        and if for whatever reason, you do not see positive results within 14
        days,<br>
        just send us a message and we’ll refund you the full amount,<br>
        no questions asked!
      </div>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'GuaranteeComponent'
}
</script>

<style scoped>
.guarantee-section {
  text-align: center;
  background: #bf8876;
  padding: 60px 0;
}
.guarantee-section_text{
    margin-top: 40px;
    font-size: 30px;
    color: #fff;
    font-family: 'Roboto';
    text-align: center;
}
</style>
