<template>
  <!-- Here is the landing page-->
  <div>
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
import { largeCardSections, smallCardSections } from "@/assets/data.js";
export default {
  data() {
    return {
      //associate the largeCardInfo with the data.js, then pass the data as props to the component
      largeCardInfo: largeCardSections,
      smallCardSections: smallCardSections,
    };
  },
};
</script>
