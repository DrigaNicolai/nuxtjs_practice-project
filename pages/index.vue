<script>
import { largeCardSections, smallCardSections } from '~/assets/data.js'
export default {
  name: 'IndexPage',

  data: () => ({
    largeCardInfo: largeCardSections,
    smallCardInfo: smallCardSections
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
    <SmallCardDisplay
      v-for="cardInfo in smallCardInfo"
      :key="cardInfo.id"
      :cards-section="cardInfo"
    />
  </div>
</template>
