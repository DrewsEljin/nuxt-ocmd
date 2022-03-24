<template>
  <section class="first-screen">
    <v-container v-view>
      <div class="first-screen_text">
        <h2 class="first-screen_title">
          Tired Of "Miracle Creams" That Promise To Be The Secret <br>
          <a class="first-screen_title_italic">"Fountain Of Youth"</a> Yet End
          Up Being a Complete Waste?
        </h2>
        <div class="first-screen_advice">
          Continue Reading to Find Why 100,000+ Women Say OCMD™ Products are the
          Only Ones that Work. <br> <a class="first-screen_advice_italic">Risk-FREE, No Strings Attached</a>  (no autobills, no
          autoships)
        </div>
        <div class="first-screen_hint">
          A Hint – it has to do with years of research and using 30+
          clinically-proven natural-based ingredients. Keep Reading…
        </div>
      </div>
    </v-container>
    <div v-view class="first-screen_images">
      <div v-view="viewHandler" :class="{ active: inview }" class="first-screen_cream">
        <img src="@/assets/images/vector_2.png" alt="">
        <img src="@/assets/images/vector_1.png" alt="">
        <img src="@/assets/images/cream.png" alt="">
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'FirstScreen',
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
section.first-screen {
  display: flex;
  flex-direction: column;
}
h2.first-screen_title {
  font-family: "PlayfairDisplayRegular";
  font-size: 30px;
  color: #54595f;
  text-align: center;
}
.first-screen_title_italic {
  font-family: "PlayfairDisplayBold";
  font-style: italic;
  color: #bf8876;
}
.first-screen_advice {
  font-family: "Roboto";
  font-size: 23px;
  color: #54595f;
  font-weight: normal;
  text-align: center;
  margin: 25px 0;
}

.first-screen_advice_italic{
  text-decoration: underline;
  font-style: italic;
  color: #bf8876;
}

.first-screen_images {
  flex: 1 1 auto;
  margin-top: 60px;
  background-image: url('@/assets/images/bg_first.png');
  background-position: bottom;
  display: flex;
  justify-content: center;
  text-align: center;
  position: relative;
}
.first-screen_hint {
  font-family: "Roboto";
  color: #54595f;
  text-align: center;
  font-size: 20px;
  padding: 15px 0;
  background: #F3F3F3;
  border-radius: 15px;
}
.first-screen_cream {
 display: flex;
 align-items: flex-end;
 justify-content: center;
 position: relative;
 height: 450px;
 width: 450px;
 opacity: 0;
 transition: 0.7s;
}
.first-screen_cream.active {
  opacity: 1;
  padding-bottom: 78px;
}

.first-screen_cream img{
  position: absolute;
  max-height: 100%;
  max-width: 100%;
}

</style>
