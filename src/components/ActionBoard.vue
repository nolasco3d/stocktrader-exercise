<template>
  <v-card flat outlined>
    <v-toolbar flat dense color="green" class="white--text">
      <div class="d-flex align-center justify-center">
        <h6 class="text-h6 mr-2">{{ name }}</h6>
        <span class="d-inline text-caption">(Preço: R$ {{ price }})</span>
      </div>
    </v-toolbar>
    <v-card-text>
      <div class="row">
        <div class="col">
          <v-text-field
            v-model="amount"
            :rules="[rules.minvalue, rules.maxLength]"
            label="Amount"
            type="number"
          />
        </div>
        <div class="col-auto d-flex align-center">
          <v-btn depressed>Click</v-btn>
        </div>
      </div>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      rules: {
        minvalue: (v) => v >= 0 || "Do not input negative values",
        maxLength: (v) => (v.length <= 6 && v <= 999999) || "Maximum amount",
      },
    };
  },
  props: {
    name: {
      type: String,
      default: "Action Name",
    },
    description: {
      type: String,
      default: "My description here",
    },
    amount: {
      type: Number,
      default: 0,
    },
    price: {
      type: Number,
      default: 0,
    },
  },
};
</script>

<style></style>
