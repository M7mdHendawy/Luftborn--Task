<template>
  <div class="griddy">
    <div class="wrapper" v-for="card in cards" :key="card.id">
      <div class="wrapper_card">
        <div class="row">
          <h2>{{ card.category }}</h2>
          <button><img src="../assets/CombinedShape.png" alt="CombinedShape" /></button>
        </div>
        <div class="row--title">
          <h3>{{ card.price }}$</h3>
          <div class="row">
            <p class="title">{{ card.title }}</p>
            <div class="InStore">
              <p>InStore</p>
              <p>{{ card.rating.count }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import axios from "axios";

export default {
  name: "SingleCard",
  data() {
    return {
      cards: [],
    };
  },
  created() {
    axios.get("https://fakestoreapi.com/products?limit=10").then((response) => {
      console.log(response.data);
      this.cards = response.data;
    });
  },
};
</script>

<style lang="scss">

</style>
