<script>
import { mapState } from "vuex";
export default {
  name: 'MyItems',

  layout: "no-nav",

  computed: {
    ...mapState(['myRentals'])
  }
}
</script>

<template>
  <div class="container">
    <MyItem
      v-for="rental in myRentals"
      :key="rental.id"
      :item="rental"
    />
  </div>
</template>

<style scoped>
.container {
  padding: 5rem 0
}
</style>
