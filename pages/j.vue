
 

<template>
    <v-card>
      <v-app-bar
        flat
        absolute
        color="#43a047"
        dark
        shrink-on-scroll
        prominent
        src="https://picsum.photos/1920/1080?random"
        fade-img-on-scroll
        scroll-target="#scrolling-techniques-5"
        scroll-threshold="500"
      >
        <template v-slot:img="{ props }">
          <v-img
            v-bind="props"
            gradient="to top right, rgba(55,236,186,.7), rgba(25,32,72,.7)"
          ></v-img>
        </template>
        <v-app-bar-title class="my-center">Download</v-app-bar-title>
  
        <v-spacer></v-spacer>
        <v-row>
          <v-col cols="6"></v-col>
          <v-col cols="6" align="right" justify="center">
            <v-card
              style="border-radius: 5px"
              flat
              max-width="180px"
              @mouseleave="detOutlined(null)"
            >
              <v-list class="pa-0 text-center">
                <v-list-group
                  style="border-radius: 5px"
                  @mouseenter="show = false"
                  :style="{
                    backgroundColor:
                      show === null ? 'rgb(191, 191, 191)' : 'rgb(242, 242, 242)',
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
          </v-col>
        </v-row>
      </v-app-bar>
      <v-sheet
        id="scrolling-techniques-5"
        class="overflow-y-auto"
        max-height="900"
      >
        <v-card>
          <v-row>
            <v-col cols="12" sm="10">
              <v-card outlined>
                <v-simple-table max-height="450px">
                  <template v-slot:default>
                    <thead>
                      <tr style="background-color: #ff3333">
                        <th style="color: #fff" class="text-left">Currency</th>
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
                        <td class="text-left">
                          <v-row>
                            <v-col cols="6" align="center">
                              <v-card-actions>
                                <div style="height: 35px; width: 35px">
                                  <v-img
                                    style="
                                      border-radius: 50%;
                                      height: 100%;
                                      width: 100%;
                                    "
                                    :src="item.image"
                                  />
                                </div>
                                <div class="pl-4">
                                  {{ item.Currency }}
                                </div>
                              </v-card-actions>
                            </v-col>
                            <v-col cols="6"></v-col>
                          </v-row>
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
        </v-card>
      </v-sheet>
    </v-card>
  </template>
  <script>
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
            image: "https://iblaos.com/iblaos/image/rate/usd.png",
          },
          {
            Currency: "TBM",
            Sell: 202,
            Buy: 237,
            image: "https://iblaos.com/iblaos/image/rate/thb.png",
          },
          {
            Currency: "TBM",
            Sell: 202,
            Buy: 237,
            image: "https://iblaos.com/iblaos/image/rate/thb.png",
          },
          {
            Currency: "TBM",
            Sell: 202,
            Buy: 237,
            image: "https://iblaos.com/iblaos/image/rate/thb.png",
          },
          {
            Currency: "TBM",
            Sell: 202,
            Buy: 237,
            image: "https://iblaos.com/iblaos/image/rate/thb.png",
          },
          {
            Currency: "TBM",
            Sell: 202,
            Buy: 237,
            image: "https://iblaos.com/iblaos/image/rate/thb.png",
          },
          {
            Currency: "TBM",
            Sell: 202,
            Buy: 237,
            image: "https://iblaos.com/iblaos/image/rate/thb.png",
          },
          {
            Currency: "TBM",
            Sell: 202,
            Buy: 237,
            image: "https://iblaos.com/iblaos/image/rate/thb.png",
          },
          {
            Currency: "TBM",
            Sell: 202,
            Buy: 237,
            image: "https://iblaos.com/iblaos/image/rate/thb.png",
          },
          {
            Currency: "TBM",
            Sell: 202,
            Buy: 237,
            image: "https://iblaos.com/iblaos/image/rate/thb.png",
          },
          {
            Currency: "TBM",
            Sell: 202,
            Buy: 237,
            image: "https://iblaos.com/iblaos/image/rate/thb.png",
          },
          {
            Currency: "TBM",
            Sell: 202,
            Buy: 237,
            image: "https://iblaos.com/iblaos/image/rate/thb.png",
          },
          {
            Currency: "GBP",
            Sell: 202,
            Buy: 262,
            image: "https://iblaos.com/iblaos/image/rate/gbp.png",
          },
          {
            Currency: "JPY",
            Sell: 202,
            Buy: 262,
            image: "https://iblaos.com/iblaos/image/rate/gbp.png",
          },
          {
            Currency: "AUD",
            Sell: 202,
            Buy: 262,
            image: "https://iblaos.com/iblaos/image/rate/aud.png",
          },
          {
            Currency: "CAD",
            Sell: 202,
            Buy: 200,
            image: "https://iblaos.com/iblaos/image/rate/cad.png",
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
    },
  };
  </script>
  
  