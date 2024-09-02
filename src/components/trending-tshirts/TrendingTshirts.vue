<template>
  <div>
    <div class="d-flex justify-center align-center">
      <hr class="seprator" />
      <h2 class="mx-4">Trending T-Shirts</h2>
      <hr class="seprator" />
    </div>
    <div class="card-container">
      <div v-for="data in cardData" :key="data.id">
        <store-card :cardData="data" />
      </div>
    </div>
  </div>
</template>
<script>
import StoreCard from "@/components/common/StoreCard.vue";
export default {
  name: "TrendingTshirts",

  components: {
    StoreCard,
  },

  data() {
    return {
      cardData: [
        {
          id: 1,
          subtitle: "Subtitle 1",
          description: "Description ",
          discountedPrize: 900,
          maximumRetailPrize: 1200,
          imageURL: require("@/assets/images/trending-tshirts/t-shirt1.svg"),
        },
        {
          id: 2,
          subtitle: "Subtitle 2",
          description: "Description 2",
          discountedPrize: 800,
          maximumRetailPrize: 1100,
          imageURL: require("@/assets/images/trending-tshirts/t-shirt2.svg"),
        },
        {
          id: 3,
          subtitle: "Subtitle 3",
          description: "Description 3",
          discountedPrize: 700,
          maximumRetailPrize: 1000,
          imageURL: require("@/assets/images/trending-tshirts/t-shirt3.svg"),
        },
        {
          id: 4,
          subtitle: "Subtitle 4",
          description: "Description 4",
          discountedPrize: 600,
          maximumRetailPrize: 900,
          imageURL: require("@/assets/images/trending-tshirts/t-shirt4.svg"),
        },
        {
          id: 5,
          subtitle: "Subtitle 5",
          description: "Description 5",
          discountedPrize: 850,
          maximumRetailPrize: 1300,
          imageURL: require("@/assets/images/trending-tshirts/t-shirt1.svg"),
        },
        {
          id: 6,
          subtitle: "Subtitle 6",
          description: "Description 6",
          discountedPrize: 950,
          maximumRetailPrize: 1400,
          imageURL: require("@/assets/images/trending-tshirts/t-shirt2.svg"),
        },
        {
          id: 7,
          subtitle: "Subtitle 7",
          description: "Description 7",
          discountedPrize: 720,
          maximumRetailPrize: 1050,
          imageURL: require("@/assets/images/trending-tshirts/t-shirt3.svg"),
        },
        {
          id: 8,
          subtitle: "Subtitle 8",
          description: "Description 8",
          discountedPrize: 880,
          maximumRetailPrize: 1250,
          imageURL: require("@/assets/images/trending-tshirts/t-shirt4.svg"),
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.seprator {
  width: 36%;
}
.card-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
}
</style>
