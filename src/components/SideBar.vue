<template>
  <v-navigation-drawer app dark color="#2A3042">
    <div class="text-center mt-5">
      <v-img class="mx-auto" src="@/assets/logowhite.png" width="150px"></v-img>
    </div>

    <v-list flat style="padding-top: 30px">
      <v-list-item-group v-model="selectedItem" color="white">
        <v-list-item color="#A6B0CF" link to="/Dashboard">
          <v-list-item-icon>
            <v-icon> mdi-speedometer</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>Dashboard</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-subheader>DATA</v-subheader>
        <v-list-item
          v-for="(item1, i) in items1"
          :key="i"
          color="#A6B0CF"
          :to="item1.link"
        >
          <v-list-item-icon>
            <v-icon v-text="item1.icon1"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item1.text1"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-subheader>ASSETS</v-subheader>

        <v-list-item v-for="(item2, n) in items2" :key="n" color="#A6B0CF">
          <v-list-item-icon>
            <v-icon v-text="item2.icon2"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item2.text2"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-subheader>AUTHORIZATION</v-subheader>

        <v-list-item v-for="(item3, a) in items3" :key="a">
          <v-list-item-icon>
            <v-icon v-text="item3.icon3"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item3.text3"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  data: () => ({
    selectedItem: 1,
    items1: [
      { text1: "Visualization", icon1: "mdi-centos" },
      { text1: "Case", icon1: "mdi-archive-outline" },
      { text1: "Data Set", icon1: "mdi-dns-outline" },
      {
        text1: "Data Source",
        icon1: "mdi-database-outline",
        link: "/UserManagement",
      },
      { text1: "Connection", icon1: "mdi-wifi" },
    ],
    items2: [
      { text2: "Icon", icon2: "mdi-apple-keyboard-command" },
      { text2: "Image", icon2: "mdi-image-outline" },
    ],
    items3: [
      { text3: "Account", icon3: "mdi-account-outline" },
      { text3: "Role", icon3: "mdi-shield-check-outline" },
      { text3: "Workspace", icon3: "mdi-view-quilt-outline" },
    ],
  }),
  methods: {},
};
</script>

<style>
.text-sidebar {
  font-family: "Poppins", sans-serif;
}
.list-card {
  margin-bottom: 35vh;
}
</style>
