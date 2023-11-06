<template>
  <div>
    <!-- <v-card>
      <v-btn @mouseenter="showText = true" @mouseleave="showText = false">add</v-btn>
      <div @mouseenter="showText = true" @mouseleave="showText = false">
        <v-card-text v-if="showText">
        ff
      </v-card-text>
    </div>
    </v-card> -->
    <v-window show-arrows>
      <template v-slot:prev="{ on, attrs }">
        <v-btn color="success" v-bind="attrs" v-on="on">
          <v-icon>mdi-chevron-left</v-icon>
        </v-btn>
      </template>
      <template v-slot:next="{ on, attrs }">
        <v-btn class="primary" v-bind="attrs" v-on="on"
          ><v-icon>mdi-chevron-right</v-icon></v-btn
        >
      </template>
      <v-window-item v-for="item in image" :key="`card-${item}`">
        <v-card color="grey" height="100%">
          <v-img :src="item" />
        </v-card>
      </v-window-item>
    </v-window>
    <v-row class="my-6">
      <v-col cols="6" class="px-6">
        <v-col cols="10">
          <v-img
            style="left: 20%"
            src="https://iblaos.com/iblaos/image/default/mb_banking.PNG"
          />
        </v-col>
      </v-col>
      <v-col cols="6">
        <v-card-text
          class="text-center d-flex align-center"
          style="height: 100%; text-align: center"
        >
          <v-card-text>
            <v-card-text style="width: 100%; top: 20%">
              <h1>IB COOL MOBILE BANKING APPLICATION</h1>
              <h2 class="py-2">
                360 view of customer relationship Customers are able to view all
                their relationships with the bank, may it be, savings accounts,
                current accounts, Þxeddeposits and loans.
              </h2>
              <v-btn class="my-2" style="color: yellow"> See More </v-btn>
            </v-card-text>
            <v-col>
              <v-btn style="width: 30%; height: 100%">
                <div>
                  <v-icon size="50" class="pa-0">mdi-apple</v-icon>
                </div>
                <div>
                  <v-card-text class="pa-0"> Download on the</v-card-text>
                  <v-card-text class="pa-0"> App store </v-card-text>
                </div>
              </v-btn>
              <v-btn style="width: 30%; height: 100%">
                <div>
                  <v-icon size="50" class="pa-0">mdi-apple</v-icon>
                </div>
                <div>
                  <v-card-text class="pa-0"> Download</v-card-text>
                  <v-card-text class="pa-0"> App store </v-card-text>
                </div>
              </v-btn>
              <v-btn style="width: 30%; height: 100%">
                <div>
                  <v-icon size="50" class="pa-0">mdi-apple</v-icon>
                </div>
                <div>
                  <v-card-text class="pa-0"> Download </v-card-text>
                  <v-card-text class="pa-0"> App store </v-card-text>
                </div>
              </v-btn>
            </v-col>
          </v-card-text>
        </v-card-text>
      </v-col>
    </v-row>
    <v-img
      class="my-4"
      src="https://iblaos.com/iblaos/image/default/visa_banner.jpg"
    />
    <v-card-text class="px-12 text-center">
      <div>
        Say hello to your new Indochina Bank Visa card! The Indochina Bank Visa
        card offers you unmatched privileges and rewards as you travel the
        globe. With acceptance at millions of merchants worldwide and the
        accessibility for local and overseas ATM cash withdrawals and advances,
        it's the seamless way to pay anywhere. We hope that you enjoy your
        shopping, dining and leisure experiences with this card.
      </div>
      <div class="py-4">
        <v-btn style="color: yellow"> See More </v-btn>
      </div>
      <v-row>
        <v-col cols="12">
          <v-img
            src="https://iblaos.com/iblaos/image/personal/cards/cards.png"
          />
        </v-col>
      </v-row>
    </v-card-text>

    <v-img
      style="height: 540px"
      src="https://img.freepik.com/free-photo/modern-office-with-view-city_1340-37363.jpg"
    >
      <v-row>
        <v-col cols="6">
          <v-card-text>
            <v-card-title> PREMIER BANKING </v-card-title>
            <v-card-text>
              As the pioneer in the premier banking service in Lao PDR,
              Indochina Bank's VIP Premier Banking Service is one of the Þnest
              luxury banking experience that if offered to all high net worth
              customers that comes with superior service coupled with specially
              tailored amenities.
            </v-card-text>
          </v-card-text>
        </v-col>
        <v-col cols="6">
          <v-card style="height: 80%; width: 80%">
            <v-img
              src="https://iblaos.com/iblaos/image/default/Premier_slide_2.jpg"
            />
          </v-card>
        </v-col>
      </v-row>
    </v-img>
    <v-card-text>
      <v-row>
        <v-col cols="6">
          <v-card style="height: 100%; width: 80%">
            <v-img
              src="https://iblaos.com/iblaos/image/news/20230403144915_2.jpg"
            />
            <v-card-text>
              <v-card-title>
                Payengxa Lor Official Appointment of IB Brand Ambassador
              </v-card-title>
              <v-btn style="color: yellow"> See More </v-btn>
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="6">
          <v-card text>
            <v-card-title> Exchange rate </v-card-title>
            <v-card-text> Date: 06/11/2023 </v-card-text>
            <v-data-table
              :headers="headers"
              :items="desserts"
              hide-default-footer
              class="elevation-1"
            ></v-data-table>
          </v-card>
        </v-col>
      </v-row>
    </v-card-text>
  </div>
</template>

<script>
export default {
  name: "DefaultLayout",
  data() {
    return {
      showText: false,
      image: [
        "https://iblaos.com/iblaos/image/slide/20230912154356_2.jpg",
        "https://iblaos.com/iblaos/image/slide/20230913144236_2.jpg",
        "https://iblaos.com/iblaos/image/slide/20230913145105_2.jpg",
        "https://iblaos.com/iblaos/image/slide/20230913144400_2.jpg",
        "https://iblaos.com/iblaos/image/slide/20220818163616_2.jpg",
      ],
      headers: [
          {
            text: 'Dessert ',
            align: 'start',
            filterable: false,
            value: 'name',
          },
          { text: 'Fat ', value: 'fat' },
          { text: 'Carbs ', value: 'carbs' },
        ],
        desserts: [
          {
            name: 'Frozen Yogurt',
            calories: 159,
            fat: 6.0,
            carbs: 24,
            protein: 4.0,
            iron: 1,
          },
          {
            name: 'Ice cream sandwich',
            calories: 237,
            fat: 9.0,
            carbs: 37,
            protein: 4.3,
            iron: 1,
          },
          {
            name: 'Eclair',
            calories: 262,
            fat: 16.0,
            carbs: 23,
            protein: 6.0,
            iron: 7,
          },
          {
            name: 'Cupcake',
            calories: 305,
            fat: 3.7,
            carbs: 67,
            protein: 4.3,
            iron: 8,
          },
          {
            name: 'Gingerbread',
            calories: 356,
            fat: 16.0,
            carbs: 49,
            protein: 3.9,
            iron: 16,
          },
          {
            name: 'Jelly bean',
            calories: 375,
            fat: 0.0,
            carbs: 94,
            protein: 0.0,
            iron: 0,
          },
          {
            name: 'Lollipop',
            calories: 392,
            fat: 0.2,
            carbs: 98,
            protein: 0,
            iron: 2,
          },
          {
            name: 'Honeycomb',
            calories: 408,
            fat: 3.2,
            carbs: 87,
            protein: 6.5,
            iron: 45,
          },
        ],
    };
  },
};
</script>
<style scoped>
.color_background_btn {
  background-color: blue;
  color: #fff;
}
</style>
