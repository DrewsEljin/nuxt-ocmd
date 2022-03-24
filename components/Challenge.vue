<template>
  <section v-view>
    <v-container>
      <h2>
        Inviting You to Join the <br>
        <b> 2-WEEKS CHALLENGE</b>
      </h2>
      <div class="challenge-text">
        After carefully developing our OCMD Rejuvenation Complex Cream <br>
        for over 2.5 years, using top technology and relying on the <br>
        most advanced researches in the field, We are so proud of this product
        that we offer you the chance to try out a <br>
        limited edition two-week sample.
      </div>
      <div class="challenge-text">
        <b>
          Two weeks is all the time Thousands of Our <br>
          Customers Needed to Start Seeing Visible Change! <br>
          Will You Be Our Next Success Case-Study?</b>
      </div>
      <div class="cards">
        <div class="card_item">
          <img src="@/assets/images/card1.png" alt="">
        </div>
        <div class="card_item">
          <img src="@/assets/images/card2.png" alt="">
        </div>
        <div class="card_item">
          <img src="@/assets/images/card3.png" alt="">
        </div>
        <div class="card_item">
          <img src="@/assets/images/card4.png" alt="">
        </div>
      </div>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'ChallengeComponent'
}
</script>

<style scoped>
h2 {
  font-family: "Roboto";
  color: #54595f;
  text-align: center;
  font-size: 40px;
}
h2 b {
  font-size: 50px;
  color: #0075b2;
}
.challenge-text {
  max-width: 1200px;
  font-family: "Roboto";
  text-align: center;
  font-size: 30px;
  font-style: italic;
  margin-top: 40px;
  color: #54595f;
}
.cards {
  display: grid;
  margin-top: 40px;
  grid-template-columns: auto auto auto auto;
}
.card_item {
  text-align: center;
  transition: 0.3s;
}
.card_item:hover{
  transform: scale(1.3);
}
@media (max-width: 768px) {
  .cards {
    grid-template-columns: auto auto;
  }
  h2 {
    font-size: 24px;
  }
  h2 b{
    font-size: 34px;
  }
  .challenge-text,.challenge-text{
    font-size: 14px;
  }
}
</style>
