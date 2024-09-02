<template>
  <div>
    <v-card class="overflow-hidden" width="100%">
      <v-app-bar color="white">
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        <v-spacer></v-spacer>
        <v-toolbar-title>Logo Here</v-toolbar-title>
        <v-spacer></v-spacer>

        <v-btn icon>
          <img src="@/assets/icons/search-icon.svg" alt="search-icon" />
        </v-btn>

        <v-btn icon>
          <img src="@/assets/icons/favourite-icon.svg" alt="favourite-icon" />
        </v-btn>

        <v-btn icon>
          <img src="@/assets/icons/cart-icon.svg" alt="cart-icon" />
        </v-btn>
        <v-btn icon>
          <img src="@/assets/icons/profile-icon.svg" alt="profile-icon" />
        </v-btn>
      </v-app-bar>
    </v-card>
    <v-navigation-drawer v-model="drawer" absolute bottom temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title>Search</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Favourite</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Cart</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Profile</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>
<script>
export default {
  data: () => ({
    drawer: false,
    group: null,
  }),

  watch: {
    group() {
      this.drawer = false;
    },
  },
};
</script>
<style lang="scss" scoped>
@import "@/assets/styles/styles.scss";
</style>
