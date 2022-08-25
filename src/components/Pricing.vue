<template>
  <div class="pricing">
    <div class="pricing__cards">
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

background-repeat:no-repeat;
background-image:
/* 1) elipse1    */ radial-gradient(
      50% 50% at 50% 50%,
      #ffddb6 0%,
      rgba(255, 221, 182, 0) 100%
    ),
/* 2) elipse2     */ radial-gradient(
      50% 50% at 50% 50%,
      rgba(237, 187, 255, 0.6) 0%,
      rgba(237, 187, 255, 0) 100%
    ),
/* 3) elipse3      */ radial-gradient(
      50% 50% at 50% 50%,
      #c6fcff 0%,
      rgba(198, 252, 255, 0) 100%
    );

background-position:
/* 1) elipse1     */923px  169px,
/* 2) elipse2     */-130px 316px,
/* 3) elipse3     */396px 18px;

background-size:
/* 1) elipse1      */ 624px 624px,
/* 2) elipse2      */ 1000px 1000px,
/* 3) elipse3      */528px 528px;
  &__cards {
    box-sizing: border-box;
    position: absolute;
    display: flex;
    justify-content: space-evenly;
    width: 75%;
    height: 70%;
    top: 20%;
    background: rgba(255, 255, 255, 0.7);
    border: 20px solid #ffffff;
    border-radius: 30px;
  }
}
</style>
