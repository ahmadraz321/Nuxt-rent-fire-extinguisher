<template>
    <div>
      <HeroSection />
      <div class="contain"></div>
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
import { largeCardSections, smallCardSections } from "@/assets/data.js";
export default {
  name: "IndexPage",
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardSections,
    };
  },
};
</script>

<style scoped>
.contain {
  height: 300px;
}
</style>
