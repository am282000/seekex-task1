<template>
  <v-card :loading="loading" class="mx-auto my-12" elevation="0">
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="10"
        indeterminate
      ></v-progress-linear>
    </template>

    <div
      class="image-overlay d-flex justify-center"
      @mouseover="showIcons = true"
      @mouseleave="showIcons = false"
    >
      <div :class="[{ 'blur-background': showIcons }]">
        <v-img height="412" width="264" :src="cardData.imageURL"></v-img>
      </div>
    </div>
    <!-- Icons to show on hover -->
    <div class="hover-icons" v-if="showIcons">
      <img
        src="@/assets/icons/card-icons/shopping-cart.svg"
        alt="Shopping cart"
      />
      <img
        src="@/assets/icons/card-icons/add-to-favourites.svg"
        alt="Add to favourite"
      />
      <img src="@/assets/icons/card-icons/share-icon.svg" alt="Share icon" />
    </div>

    <v-card-text class="text-center">
      <div class="text-subtitle-1">{{ cardData.subtitle }}</div>

      <div>{{ cardData.description }}</div>
    </v-card-text>

    <div class="d-flex justify-center align-center">
      <span class="mr-2">₹{{ cardData.discountedPrize }} </span>
      <small class="product-mrp">₹ {{ cardData.maximumRetailPrize }}</small>
    </div>

    <v-card-text class="d-flex justify-center">
      <v-chip-group
        v-model="selectedSize"
        active-class="deep-purple accent-4 white--text"
      >
        <v-chip v-for="size in sizes" :key="size" :value="size" class="px-3">{{
          size
        }}</v-chip>
      </v-chip-group>
    </v-card-text>
  </v-card>
</template>
<script>
export default {
  data: () => ({
    loading: false,
    selectedSize: null,
    showIcons: false,
    sizes: ["S", "M", "L", "XL", "XXL"],
  }),
  props: {
    cardData: { type: Object, default: () => ({}) },
  },
  methods: {},
};
</script>
<style lang="scss" scoped>
.product-mrp {
  text-decoration: line-through;
  color: $color-red;
}
.image-overlay {
  position: relative;
  overflow: hidden;
}

.blur-background {
  filter: blur(4px);
}

.hover-icons {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  gap: 10px;
  z-index: 10;
  opacity: 0.9;
}

.hover-icons v-icon {
  font-size: 24px;
  color: white;
  /* Adjust icon styles as needed */
}
</style>
