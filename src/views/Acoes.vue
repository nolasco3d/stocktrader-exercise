<template>
  <v-container>
    <v-row>
      <v-col>
        <ActionBoardVue :description="Teste"></ActionBoardVue>
        <ActionBoardVue />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import ActionBoardVue from "../components/ActionBoard.vue";

export default {
  components: {
    ActionBoardVue,
  },
  data() {
    return {};
  },
};
</script>

<style></style>
