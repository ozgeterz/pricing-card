<template>
  <div class="m-card">
    <p class="m-card__categories">{{card.categories}}</p>
    <p class="m-card__price">{{card.price}}</p>
    <p class="m-card__time">{{card.time}}</p>
    <p class="m-card__comment">{{card.comment}}</p>
    <button-vue :color="card.button">{{card.buttonname}}</button-vue>
  </div>
</template>

<script>
import ButtonVue from './Button.vue';
export default {
  name: "Card-Component",
  components:{ButtonVue},
  props: {
    card: {
      type: Object,
    },
  },
};
</script>

<style lang="scss" scoped>
.m-card {
  flex-direction: column;
  align-items: flex-start;
  font-style: normal;
  width: 30%;
  &__categories {
    font-family: "Merriweather";
    font-weight: 700;
    font-size: 26px;
    color: #141843;
  }
  &__price {
    font-family: "IBM Plex Sans";
    font-weight: 700;
    font-size: 62px;
  }
  &__time {
    font-family: "IBM Plex Sans";
    font-weight: 500;
    font-size: 16px;
  }
  &__comment {
    font-family: "IBM Plex Sans";
    font-weight: 500;
    font-size: 20px;
  }
}
</style>
