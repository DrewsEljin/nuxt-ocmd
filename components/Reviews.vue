<template>
  <section v-view>
    <v-container>
      <h2>Real Customers Talk About Their Results-</h2>
      <div class="reviews">
        <img src="@/assets/images/review1.png" alt="">
        <img src="@/assets/images/review2.png" alt="">
      </div>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'ReviewsComponent'
}
</script>

<style scoped>
section {
  margin-top: 40px;
}
h2 {
  color: #0075b2;
  font-family: "Roboto";
  font-size: 40px;
  text-align: center;
}
.reviews {
  margin-top: 40px;
  display: grid;
  width: 100%;
  grid-template-columns: auto auto;
  gap: 1rem 8rem;
  flex-wrap: wrap;
  font-family: "Roboto";
}

@media (max-width: 768px) {
  .reviews {
    grid-template-columns: auto;
  }
}
@media (max-width: 576px) {
  h2 {
    font-size: 30px;
  }
}
</style>
