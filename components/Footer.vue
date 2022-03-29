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
          <a href="/policy">Privacy Policy</a>  | <a href="/shipping">Shipping & Delivery </a> | <a href="/returns">Refunds & Returns</a>  | <a href="/terms">Terms and
            Conditions</a>
        </div>
        <div class="footer_support">
          <a href="mailto:support@ocmd.co">support@ocmd.co</a>
        </div>
        <div class="footer_note">
          The information presented on this website is not intended as specific
          medical advice and is not a substitute for professional treatment or
          diagnosis. These statements have not been evaluated by the Food and
          Drug Administration. This product is not intended to diagnose, treat,
          cure, or prevent any disease.
        </div>
        <div class="footer_rights">
          2022 © OCMD. All rights reserved.
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
.footer {
  margin-top: 60px;
}
.footer-container {
  padding: 40px 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.footer_policy {
  margin-top: 40px;
  margin-bottom: 20px;
  font-family: "AvantGarde Bk BT";
  font-size: 15px;
  font-weight: normal;
  color: #000;
}
.footer_support {
  font-family: "AvantGarde Bk BT";
  font-weight: 600;
  margin-bottom: 20px;
}
.footer_note {
  padding: 21px;
  font-family: "AvantGarde Bk BT";
  font-size: 16px;
  background: linear-gradient(0deg, #f9f5f4, #f9f5f4), #ffffff;
  border: 2px solid #f5eae5;
  border-radius: 10px;
}
.footer_rights {
  font-family: "AvantGarde Bk BT";
  font-size: 15px;
  margin-top: 20px;
}

@media (max-width:576px) {
  .footer_policy{
    text-align: center;
  }
  .footer_policy a{
    white-space: nowrap;
  }
}
</style>
