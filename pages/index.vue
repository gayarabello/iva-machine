<template>
  <div style="margin: 0 auto;">
    <v-row>
      <v-col class="text-center py-12">
        <h1 style="font-size: 3rem;">IVA MACHINE</h1>
      </v-col>
    </v-row>

    <v-row style="max-width: 500px; margin: 0 auto;" class="justify-center">
      <v-col class="text-center" cols="12">
        <h4 class="pb-4">TOTAL</h4>
        <v-text-field
          label="Insira aqui o valor total"
          outlined
          type="number"
          v-model="valor"
        >
        </v-text-field>
        <v-row class="justify-space-around py-4">
          <v-col style="background-color: #ebebeb;">
            <h4>IVA</h4>
            <h2>{{ calcIva.toFixed(2) }}</h2>
          </v-col>
          <v-col style="background-color: #00b54e; color: white;">
            <h4>LIMPO</h4>
            <h2>{{ semIva.toFixed(2) }}</h2>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";
import VuetifyLogo from "~/components/VuetifyLogo.vue";

export default {
  components: {
    Logo,
    VuetifyLogo
  },
  data() {
    return {
      valor: null,
      rate: 0.23,
      output: this.valor * this.rate
    };
  },

  computed: {
    calcIva: {
      get: function() {
        return this.valor * this.rate;
      },
      set: function() {
        return this.valor * this.rate;
      }
    },
    semIva() {
      return this.valor - this.calcIva;
    }
  },

  watch: {
    calcIva() {}
  }
};
</script>
