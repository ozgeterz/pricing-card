<template>
  <div class="pricing">
    <div class="pricing-elipse1"></div>
    <div class="pricing-elipse2"></div>
    <div class="pricing-elipse3"></div>
    <div class="pricing-cards">
        <Card v-for="card in cardList" :card="card" :key="card.price" />
    </div>
  </div>
</template>
<script>
import Card from "./Card.vue";
export default {
  name: "Pricing-Component",
  components: { Card },
  data() {
    return {
      cardList: [
        {
          categories: "Free",
          price: "$3",
          time: "Per user per mounth",
          comment: "For teams that need to manage more work",
          button: "button1",
          buttonname: "Get Started",
        },
        {
          categories: "Standart",
          price: "$6",
          time: "Per user per mounth",
          comment: "For teams that need to manage more work",
          button: "button2",
          buttonname: "Upgrade Now",
        },
        {
          categories: "Premium",
          price: "$12",
          time: "Per user per mounth",
          comment: "Best for teams that need to track multiple project",
          button: "button3",
          buttonname: "Try for free",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.pricing {
  position: relative;
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  background: #ffff;

  &-elipse1 {
    position: absolute;
    width: 624px;
    height: 624px;
    left: 923px;
    top: 169px;
    background: radial-gradient(
      50% 50% at 50% 50%,
      #ffddb6 0%,
      rgba(255, 221, 182, 0) 100%
    );
  }
  &-elipse2 {
    position: absolute;
    width: 1000px;
    height: 1000px;
    left: -130px;
    top: 316px;
    background: radial-gradient(
      50% 50% at 50% 50%,
      rgba(237, 187, 255, 0.6) 0%,
      rgba(237, 187, 255, 0) 100%
    );
  }
  &-elipse3 {
    position: absolute;
    width: 528px;
    height: 528px;
    left: 396px;
    top: 18px;
    background: radial-gradient(
      50% 50% at 50% 50%,
      #c6fcff 0%,
      rgba(198, 252, 255, 0) 100%
    );
  }
  &-cards {
    box-sizing: border-box;
    position: absolute;
    display: flex;
    justify-content: space-evenly;
    width: 75%;
    height: 70%;
    top: 40%;
    background: rgba(255, 255, 255, 0.7);
    border: 20px solid #ffffff;
    border-radius: 30px;
  }
}
</style>
