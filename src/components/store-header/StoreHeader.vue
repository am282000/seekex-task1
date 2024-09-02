<template>
  <div class="header-container">
    <div class="d-flex justify-space-around">
      <span> Welcome to Our Store Hiscraves </span>
      <span>
        <img src="@/assets/images/headerPhoneNo.svg" alt="" />
      </span>
    </div>
  </div>
</template>
<script>
export default {
  name: "StoreHeader",
};
</script>
<style lang="scss" scoped>
@import "@/assets/styles/styles.scss";

.header-container {
  background-color: $color-black;
  color: $color-white;
}
</style>
