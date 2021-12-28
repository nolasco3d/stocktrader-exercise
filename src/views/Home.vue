<template>
  <v-container>
    <v-row>
      <v-col>
        <h3>Negocie e Consule suas Ações</h3>

        <v-alert dense type="info">
          <h5>Alerta 1</h5>
        </v-alert>

        <v-alert dense type="info" color="success">
          <h5>Alerta 2</h5>
        </v-alert>

        <v-divider></v-divider>

        <h3>Seu Saldo: R$ {{ retornaSaldo }}</h3>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Home",
  components: {},
  data() {
    return {
      saldo: 10000,
    };
  },
  computed: {
    retornaSaldo() {
      return this.saldo;
    },
  },
};
</script>
