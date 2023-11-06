<template>
    <v-app dark>
      <v-app-bar flat app class="color_background">
        <v-row>
          <v-col cols="4" class="px-0">
            <v-btn
              text
              class="pa-0 ma-0"
              style="width: 100%; height: 100%; border-radius: 0%"
            >
              <v-app-bar flat style="background-color: #9925be">
                <div class="pr-2">
                  <v-img
                    style="max-width: 55px"
                    src="https://img.freepik.com/free-vector/bird-colorful-logo-gradient-vector_343694-1365.jpg"
                  />
                </div>
                <v-divider vertical style="background-color: black"></v-divider>
                <div class="px-2">
                  <v-card-text class="pa-0 color_background">
                    ທະນາຄານອິນໂດຈີນ
                  </v-card-text>
                  <v-card-text class="pa-0 color_background">
                    INDOCHINA BANK
                  </v-card-text>
                </div>
              </v-app-bar>
            </v-btn>
          </v-col>
          <v-col cols="8" class="px-0">
            <v-col style="width: 100%; height: 100%" class="color_background">
              <v-row
                style="width: 100%; height: 100%"
                class="color_background"
                outlined
              >
                <v-col
                  cols="2"
                  class="color_background pa-0"
                  style="width: 100%; height: 160%"
                >
                  <v-card @mouseenter="showText = 't'" @mouseleave="showText = 'n'" style="width: 100%; height: 100%;" flat class="pa-0 rounded-0">
                    <v-btn
                      class="color_background"
                      
                      text
                      style="width: 100%; height: 100%; border-radius: 0%"
                    >
                      s
                    </v-btn>
                  </v-card>
                </v-col>
              </v-row>
            </v-col>
          </v-col>
        </v-row>
      </v-app-bar>
      <v-main>
        <v-col
          v-if="showText == 't'"
          class="pa-0 px-5"
          style="top: 68px; position: fixed; z-index: 100"
        >
        <div @mouseenter="showText = 't'" @mouseleave="showText = 'n'">
  
          <v-card-text class="pa-0">
            <v-col class="pa-0">
              <v-row>
                <v-col
                  cols="4"
                  class="pa-0"
                  style="background-color: rgb(255, 128, 0)"
                ></v-col>
                <v-col
                  cols="8"
                  class="pa-0"
                  style="background-color: rgb(255, 128, 0)"
                >
                  <v-col style="width: 100%; height: 100%" class="py-0">
                    <v-row style="width: 100%; height: 100%" outlined>
                      <v-col
                        cols="2"
                        class="text-center pa-1"
                        :key="i"
                        style="width: 100%; height: 160%"
                      >
                        <v-icon
                          color="rgb(255, 128, 0)"
                          style="bottom: 6px"
                          v-if="showText == 't'"
                          >mdi-triangle-small-up</v-icon
                        >
                      </v-col>
                    </v-row>
                  </v-col>
                </v-col>
              </v-row>
            </v-col>
          </v-card-text>
        </div>
  
        </v-col>
  
        <v-container>
          <Nuxt />
        </v-container>
      </v-main>
    </v-app>
  </template>
  
  <script>
  export default {
    name: "DefaultLayout",
    data() {
      return {
        items: [
          { title: "about", text: "Bank" },
          { title: "personal", text: "Banking" },
          { title: "corporate", text: "Banking" },
          { title: "premier", text: "Banking" },
          { title: "reward", text: "Program" },
          { title: "cool", text: "Lifestyle" },
        ],
        showText: "n",
      };
    },
  };
  </script>
  <style scoped>
  .color_background {
    background-color: #9925be;
    color: #fff;
  }
  </style>
  