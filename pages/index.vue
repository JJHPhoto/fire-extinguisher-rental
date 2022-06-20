<template>
  <div class="container">
    <Hero />
    <LargeCardDisplay 
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    />
    <SmallCardDisplay 
      v-for="cardInfo in smallCardSections"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    />
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js"
import SmallCardDisplay from "../components/SmallCardDisplay.vue"

export default {
    data() {
        return {
            largeCardInfo: largeCardSections,
            smallCardSections
        };
    },
    components: { SmallCardDisplay }
}
</script>
