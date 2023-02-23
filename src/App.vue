<template>
  <div class="container">
    <div class="row">
      <MainCard />
      <SingleCard />
    </div>
  </div>
</template>

<script>
import SingleCard from './components/Card.vue'
import MainCard from './components/MainCard.vue'
export default {
  name: 'App',
  components: {
    SingleCard,
    MainCard
  }
}
</script>

<style lang="scss">
@import "style.scss"
</style>
