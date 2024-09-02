<template>
  <div class="hot-deals-container">
    <div class="row">
      <div v-for="image in firstRow" :key="`firstRow${image.id}`">
        <img :src="image.url" :alt="image.description" class="row1" />
      </div>
    </div>
    <div class="row">
      <div v-for="image in secondRow" :key="`secondRow${image.id}`">
        <img :src="image.url" :alt="image.description" class="row2" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstRow: [
        {
          id: 1,
          description: "Baggy UPTO 60% OFF",
          url: require("@/assets/images/hot-deals-images/hot-deals1.svg"),
        },
        {
          id: 2,
          description: "Winter Collection",
          url: require("@/assets/images/hot-deals-images/hot-deals2.svg"),
        },
      ],
      secondRow: [
        {
          id: 3,
          description: "Women's Wear",
          url: require("@/assets/images/hot-deals-images/hot-deals3.svg"),
        },
        {
          id: 4,
          description: "Best Deal UPTO 81% OFF",
          url: require("@/assets/images/hot-deals-images/hot-deals4.svg"),
        },
        {
          id: 5,
          description: "Trendy T-Shirts",
          url: require("@/assets/images/hot-deals-images/hot-deals5.svg"),
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.hot-deals-container {
  display: flex;
  flex-direction: column;
  margin: 0 6rem;
}

.row {
  display: flex;
  width: 100%;
  justify-content: space-between;
  .row1 {
    width: 40rem;
  }
  .row2 {
    width: 27rem;
  }
}
</style>
