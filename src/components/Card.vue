<template>
  <div class="card">
    <p class="card-categories">{{card.categories}}</p>
    <p class="card-price">{{card.price}}</p>
    <p class="card-time">{{card.time}}</p>
    <p class="card-comment">{{card.comment}}</p>
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
.card {
  flex-direction: column;
  align-items: flex-start;
  font-style: normal;
  width: 30%;
  &-categories {
    font-family: "Merriweather";
    font-weight: 700;
    font-size: 26px;
    color: #141843;
  }
  &-price {
    font-family: "IBM Plex Sans";
    font-weight: 700;
    font-size: 62px;
  }
  &-time {
    font-family: "IBM Plex Sans";
    font-weight: 500;
    font-size: 16px;
  }
  &-comment {
    font-family: "IBM Plex Sans";
    font-weight: 500;
    font-size: 20px;
  }
}
</style>
