<script>
import { largeCardSections } from '@/assets/data.js'
export default {
  name: 'IndexPage',

  data: () => ({
    largeCardInfo: largeCardSections
  })
}
</script>

<template>
  <div>
    <HeroComponent />
    <LargeCardDisplay
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cards-section="cardInfo"
    />
  </div>
</template>
