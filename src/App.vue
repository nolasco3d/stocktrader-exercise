<template>
  <v-app>
    <v-app-bar dense app elevation="4">
      <span><strong>STOCK</strong>TRADER</span>

      <v-tabs color="grey darken-3">
        <v-tab to="/">Home</v-tab>
        <v-tab to="/portfolio">Portfólio</v-tab>
        <v-tab to="/acoes">Ações</v-tab>
      </v-tabs>

      <v-spacer></v-spacer>
    </v-app-bar>
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>
