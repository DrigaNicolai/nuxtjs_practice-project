<script>
export default {
  name: 'SmallCard',

  props: {
    card: {
      type: Object,
      required: true
    }
  }
}
</script>

<template>
  <NuxtLink :to="`/products/${card.id}`" class="card-container">
    <img :src="require(`~/assets/images/${card.image || 'fe1.jpg'}`)" alt="small card" class="image">
  </NuxtLink>
</template>

<style scoped>
.card-container {
  width: 24%;
  height: 12.5rem;
  border-radius: 0.5rem;
  overflow: hidden;
  margin-bottom: 1.5rem;
  cursor: pointer;
}
.image {
  width: 100%;
  height: 100%
}
</style>
