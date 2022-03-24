<template>
  <div>
    <FirstScreen />
    <Reviews />
    <Offer />
    <Result />
    <Challenge />
    <Rejuvenation />
    <Guarantee />
    <Instruction />
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>

<style >
.tns-nav button {
  display: block !important;
  border: 2px solid #ef7868;
  opacity: 1;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  margin: 40px 6px 0 6px !important;
}
.tns-nav-active {
  background: #ef7868;
}
.tns-nav {
  position: absolute;
  left: 50%;
  transform: translate(-50%);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.tns-item {
  text-align: center;
}
.tns-outer .tns-controls {
  position: absolute;
  z-index: 2;
  top: 50%;
  width: 100%;
}
.tns-outer {
  position: relative;
}
.tns-outer .tns-controls button {
  position: absolute;
  top: 0;
  border: none;
  font-size: 0;
  background-image: url("@/assets/images/arrow-left.png");
  width: 40px;
  height: 40px;
  padding: 0;
  z-index: 2;
}
.tns-outer .tns-controls button[data-controls="next"] {
  transform: rotateY(180deg);
  right: 0;
}
img {
  max-width: 100%;
}

@media (max-width:768px) {
  .tns-outer .tns-controls{
    display: none;
  }
}
</style>
