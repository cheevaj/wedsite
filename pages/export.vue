<template>
  <div>
    <v-row>
      <v-col cols="12" sm="10">
        <v-card flat class="rounded-0" min-height="50px"> </v-card>
      </v-col>
      <v-col cols="2">
        <v-card
          max-width="180px"
          style="position: fixed; z-index: 100; right: 10px"
          flat
          min-width="100px"
        >
          <v-card outlined width="100%" @mouseleave="detOutlined(null)">
            <v-list class="pa-0 text-center">
              <v-list-group
                @mouseenter="show = false"
                :style="{
                  backgroundColor:
                    show === null ? 'rgb(217, 217, 217)' : '#ffffff',
                }"
              >
                <template v-slot:activator>
                  <v-card-text class="pa-0"> Download </v-card-text>
                  <v-icon class="pl-1 pb-1">mdi-tray-arrow-up</v-icon>
                </template>
                <v-col>
                  <v-btn
                    class="mt-2"
                    text
                    height="25%"
                    width="100%"
                    small
                    @mouseenter="setOutlined('button1')"
                    @mouseleave="detOutlined(true)"
                    @click="exportToExcel"
                    color="#009933"
                    :style="{
                      boxShadow: show ? '#00ff55' : 'rgb(217, 217, 217)',
                    }"
                    :outlined="show === 'button1' ? false : true"
                  >
                    <v-icon
                      style="background-color: #009933; border-radius=50%"
                      size="35"
                      color="#ffffff"
                      >mdi-microsoft-excel</v-icon
                    >
                    <v-card-text
                      :style="{
                        color: show === 'button1' ? '#009933' : '#000',
                      }"
                      >Excel</v-card-text
                    >
                  </v-btn>

                  <v-btn
                    class="mt-2"
                    text
                    height="25%"
                    width="100%"
                    small
                    @mouseenter="setOutlined('button2')"
                    @mouseleave="detOutlined(true)"
                    color="#ff3333"
                    :style="{
                      boxShadow: show ? '#00ff55' : 'rgb(217, 217, 217)',
                    }"
                    :outlined="show === 'button2' ? false : true"
                  >
                    <v-icon
                      style="background-color: #ff3333; border-radius=50%"
                      size="35"
                      color="#ffffff"
                      >mdi-file-code-outline</v-icon
                    >
                    <v-card-text
                      :style="{
                        color: show === 'button2' ? '#ff3333' : '#000',
                      }"
                      >Csv</v-card-text
                    >
                  </v-btn>
                </v-col>
              </v-list-group>
            </v-list>
          </v-card>
        </v-card>
      </v-col>
    </v-row>

    <v-row>
      <v-col cols="12" sm="10">
        <v-card outlined>
          <v-simple-table max-height="450px">
            <template v-slot:default>
              <thead>
                <tr style="background-color: #ff3333">
                  <th style="color: #fff" class="text-center">Currency</th>
                  <th style="color: #fff" class="text-center">Buy</th>
                  <th style="color: #fff" class="text-center">Sell</th>
                </tr>
              </thead>
              <tbody>
                <tr
                  v-for="(item, index) in desserts"
                  :key="item.Currency"
                  :style="{
                    backgroundColor:
                      index % 2 == 0 ? 'rgb(242, 242, 242)' : '#ffffff',
                  }"
                >
                  <td class="text-center">
                    {{ item.Currency }}
                  </td>
                  <td class="text-center">{{ item.Buy }}.00</td>
                  <td class="text-center">{{ item.Sell }}.00</td>
                </tr>
              </tbody>
            </template>
          </v-simple-table>
        </v-card>
      </v-col>
      <v-col class="px-0" sm="2"> </v-col>
    </v-row>
  </div>
</template>
<script>
import * as XLSX from 'xlsx';
export default {
  Currency: "DefaultLayout",
  data() {
    return {
      show: null,
      onboarding: 0,
      onboarding1: 0,
      color: "#e5e5e5",
      desserts: [
        {
          Currency: "USD",
          Buy: "20,680",
          Sell: "20.812",
        },
        {
          Currency: "TBM",
          Sell: 202,
          Buy: 237,
        },
        {
          Currency: "TBM",
          Sell: 202,
          Buy: 237,
        },
        {
          Currency: "TBM",
          Sell: 202,
          Buy: 237,
        },
        {
          Currency: "TBM",
          Sell: 202,
          Buy: 237,
        },
        {
          Currency: "TBM",
          Sell: 202,
          Buy: 237,
        },
        {
          Currency: "TBM",
          Sell: 202,
          Buy: 237,
        },
        {
          Currency: "TBM",
          Sell: 202,
          Buy: 237,
        },
        {
          Currency: "TBM",
          Sell: 202,
          Buy: 237,
        },
        {
          Currency: "TBM",
          Sell: 202,
          Buy: 237,
        },
        {
          Currency: "TBM",
          Sell: 202,
          Buy: 237,
        },
        {
          Currency: "TBM",
          Sell: 202,
          Buy: 237,
        },
      ],
    };
  },
  methods: {
    setOutlined(value) {
      this.show = value;
    },
    detOutlined(value) {
      this.show = value;
    },
    exportToExcel() {
      const workbook = XLSX.utils.book_new();
      const worksheet = XLSX.utils.json_to_sheet(this.desserts);

      XLSX.utils.book_append_sheet(workbook, worksheet, 'Currency Data');

      // Generate a unique filename or use a timestamp for the file
      const filename = `currency_data_${Date.now()}.xlsx`;

      XLSX.writeFile(workbook, filename);
    },
  },
};
</script>