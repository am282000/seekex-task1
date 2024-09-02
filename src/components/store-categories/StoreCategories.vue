<template>
  <div class="d-flex justify-space-around mx-10 my-10">
    <v-card elevation="0" v-for="image in images" :key="image.id">
      <v-img width="200" :src="image.url" :alt="`Image${image.id}`"></v-img>
      <p class="text-center font-weight-bold">{{ image.description }}</p>
    </v-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        {
          id: 1,
          description: "Men's T-Shirts",
          url: require("@/assets/images/categories-images/categories1.svg"),
        },
        {
          id: 2,
          description: "Women's Wear",
          url: require("@/assets/images/categories-images/categories2.svg"),
        },
        {
          id: 3,
          description: "Winter Collections",
          url: require("@/assets/images/categories-images/categories3.svg"),
        },
        {
          id: 4,
          description: "Hooded T-Shirts",
          url: require("@/assets/images/categories-images/categories4.svg"),
        },
        {
          id: 5,
          description: "Polo Neck T-Shirts",
          url: require("@/assets/images/categories-images/categories5.svg"),
        },
        {
          id: 6,
          description: "Full Sleeves T-Shirts",
          url: require("@/assets/images/categories-images/categories6.svg"),
        },
      ],
    };
  },
};
</script>
