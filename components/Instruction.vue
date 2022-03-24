<template>
  <section class="instruction-section">
    <v-container>
      <div v-view class="instruction-section_block">
        <h2>How to use?</h2>
        <img src="@/assets/images/instruction1.png" alt="">
      </div>
      <div v-view class="instruction-section_block">
        <h2>What can you expect?</h2>
        <div class="instruction-section_block__text">
          During the first week you might experience a tingling sensation, which
          means the active ingredients in our formula are doing their job. Your
          skin will soon begin to feel smoother and healthier. After four weeks
          you will notice that your wrinkles are smaller, your skin is firmer
          and your complexion is brighter.
        </div>
      </div>
      <div v-view class="instruction-section_block">
        <h2>The Science Behind</h2>
        <div class="instruction-section_block_science">
          <img src="@/assets/images/science.png" alt="">
          <div class="instruction-section_block_science_text">
            <p>
              OCMD Rejuvenation Complex Cream uses a combination of 3 sizes of
              Hyaluronic Acid molecules and a hand picked selection of 17 active
              ingredients, including apple stem cells extracts, vitamin
              liposomes, and natural compounds like lactic acid.
            </p>
            <p>
              Our formula gently exfoliates the epidermis and penetrates into
              the lower skin levels to optimize product efficiency.
            </p>
            <p>
              The Shrunken Hyaluronic Acid molecules trap moisture. The Swiss
              Apple Stem Cells Increase skin stem cell regeneration by 80% and
              reduce the damage of UV sun light on skin stem cells by 46%. The
              vitamin liposomes nourish the skin. Other active ingredients
              trigger and enhance Elastin & Collagen production. The result of
              all this is a tighter, smoother skin and a brighter complexion.
            </p>
          </div>
        </div>
      </div>
      <div v-view class="instruction-section_block">
        <h2>Full Ingredients List</h2>
        <div class="instruction-section_block_list">
          WATER; ISOPROPYL MYRISTATE; RICINUS COMMUNIS (CASTOR) SEED OIL;
          SQUALANE; CYCLOPENTASILOXANE; DIMETHICONE; CAPRYLIC/CAPRIC
          TRIGLYCERIDE; GLYCERIN; TOCOPHERYL ACETATE; SODIUM ACRYLATE / SODIUM
          ACRYLOYLDIMETHYL TAURATE COPOLYMER; PHENOXYETHANOL; PANTHENOL; RETINYL
          PALMITATE; ISOHEXADECANE; POLYSORBATE 20; TITANIUM DIOXIDE; MATRICARIA
          CHAMOMILLA (GERMAN CHAMOMILE) FLOWER WATER; SODIUM BENZOATE; CALENDULA
          OFFICINALIS (CALENDULA) FLOWER WATER; POLYSORBATE 80; PERSEA
          GRATISSIMA (AVOCADO) OIL; TRITICUM VULGARE (WHEAT) GERM OIL;
          FRAGRANCE; SORBITAN OLEATE; MALUS DOMESTICA (APPLE) FRUIT CELL CULTURE
          EXTRACT; ALCOHOL; PRUNUS DULCIS (SWEET ALMOND) OIL;
          ETHYLHEXYLGLYCERIN; BORAGO OFFICINALIS (BORAGE) SEED OIL; SODIUM
          HYALURONATE; LECITHIN; XANTHAN GUM; BENZYL ALCOHOL; CITRIC ACID;
          ASCORBYL PALMITATE; POTASSIUM SORBATE; LINALOOK, CITRONELLOL;
          GERANIOL, LIMONENE.
        </div>
      </div>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'InstructionComponent'
}
</script>

<style scoped>
section {
  margin: 0;
}
h2 {
  font-size: 40px;
  color: #54595f;
  text-align: center;
  font-weight: normal;
  font-family: "PlayfairDisplay";
  margin-bottom: 40px;
}
.instruction-section_block {
  padding: 40px 0;
  border-bottom: 1px solid #efefef;
  text-align: center;
  font-family: 'Roboto';
}
.instruction-section_block:last-of-type{
   border-bottom: 1px solid #DADADA;
}
.instruction-section_block__text {
  text-align: left;
  color: #383838;
  font-size: 20px;
  font-weight: 300;
}
.instruction-section_block_science {
  display: flex;
  gap: 40px;
  font-size: 20px;
  font-weight: 300;
  text-align: left;
}
.instruction-section_block_science p {
  margin-bottom: 30px;
}

.instruction-section_block_list{
    text-align: left;
    font-weight: 300;
    color: #383838;
    font-size: 18px;
}
@media (max-width:990px) {
    .instruction-section_block_science{
    flex-wrap: wrap;
    justify-content: center;
}
}
</style>
