<template>
  <footer>
    <v-container>
      <div class="footer-container">
        <img
          class="footer_logo"
          src="@/assets/images/ocmd-bottom.png"
          alt=""
          srcset=""
        >
        <div class="footer_policy">
          Privacy Policy | Shipping & Delivery | Refunds & Returns | Terms and
          Conditions
        </div>
        <div class="footer_support">
          support@ocmd.co
        </div>
        <div class="footer_note">
          The information presented on this website is not intended as specific
          medical advice and is not a substitute for professional treatment or
          diagnosis. These statements have not been evaluated by the Food and
          Drug Administration. This product is not intended to diagnose, treat,
          cure, or prevent any disease.
        </div>
        <div class="footer_rights">
          2021 © OCMD. All rights reserved.
        </div>
      </div>
    </v-container>
  </footer>
</template>

<script>
export default {
  name: 'FooterComponent'
}
</script>

<style scoped>
.footer-container {
  padding: 28px 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.footer_policy {
  margin: 40px 0;
  font-family: "AvantGarde";
  font-size: 15px;
  font-weight: normal;
  color: #000;
}
.footer_support {
  font-family: "AvantGarde";
  font-weight: 600;
  margin-bottom: 20px;
}
.footer_note {
  padding: 21px;
  font-family: "AvantGarde";
  font-size: 16px;
  background: linear-gradient(0deg, #f9f5f4, #f9f5f4), #ffffff;
  border: 2px solid #f5eae5;
  border-radius: 10px;
}
.footer_rights{
   font-family: "AvantGarde";
  font-size: 15px;
  margin-top: 20px;
}
</style>
