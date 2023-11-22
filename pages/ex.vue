<template>
  <v-card text>
    <v-card-title> Exchange rate </v-card-title>
    <v-card-text class="py-0" style="color: #aca8a8">
      Date: 06/11/2023
    </v-card-text>
    <v-simple-table height="300px">
      <template v-slot:default>
        <thead>
          <tr style="background-color: rgb(102, 48, 143)">
            <th style="color: #fff" class="text-center">Currency</th>
            <th style="color: #fff" class="text-center">Buy</th>
            <th style="color: #fff" class="text-center">Sell</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in desserts" :key="item.Currency">
            <td class="text-center">{{ item.Currency }}</td>
            <td class="text-center">{{ item.Buy }}</td>
            <td class="text-center">{{ item.Sell }}</td>
          </tr>
        </tbody>
      </template>
    </v-simple-table>
  </v-card>
</template>
<script>
export default {
  Currency: "DefaultLayout",
  data() {
    return {
      desserts: [
        {
          Currency: "Frozen Yogurt",
          Buy: 159,
          Sell: 202,
        },
        {
          Currency: "Ice cream sandwich",
          Buy: 237,
        },
        {
          Currency: "Eclair",
          Buy: 262,
        },
      ],
    };
  },
};
</script>