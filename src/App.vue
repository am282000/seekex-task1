<template>
  <v-app>
    <v-main>
      <store-header />
      <navigation-bar />
      <store-banner />
      <store-categories />
      <hot-deals />
      <trending-tshirts />
      <!-- <HelloWorld /> -->
    </v-main>
  </v-app>
</template>

<script>
// import HelloWorld from "@/components/HelloWorld";
import StoreHeader from "@/components/store-header/StoreHeader";
import NavigationBar from "@/components/navigation-bar/NavigationBar";
import StoreBanner from "@/components/store-banner/StoreBanner";
import StoreCategories from "@/components/store-categories/StoreCategories";
import HotDeals from "@/components/hot-deals/HotDeals";
import TrendingTshirts from "@/components/trending-tshirts/TrendingTshirts";

export default {
  name: "App",

  components: {
    StoreHeader,
    // HelloWorld,
    NavigationBar,
    StoreBanner,
    StoreCategories,
    HotDeals,
    TrendingTshirts,
  },

  data: () => ({
    //
  }),
};
</script>
<style lang="scss">
@import "@/assets/styles/styles.scss";
</style>
