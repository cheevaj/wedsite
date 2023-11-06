<template>
  <v-app dark>
    <!-- <v-card class="overflow-hidden">
    <v-app-bar
      absolute
      color="#fcb69f"
      dark
      shrink-on-scroll
      src="https://picsum.photos/1920/1080?random"
      scroll-target="#scrolling-techniques-2"
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(19,84,122,.5), rgba(128,208,199,.8)"
        ></v-img>
      </template>

      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-app-bar-title>Title</v-app-bar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>
    <v-sheet
      id="scrolling-techniques-2"
      class="overflow-y-auto"
      max-height="600"
    >
      <v-container style="height: 1000px;"></v-container>
    </v-sheet>
  </v-card> -->
    <v-app-bar flat app class="color_background">
        <v-row>
          <v-col cols="4" class="px-0 color_background" style="height: 140px">
            <v-btn
              text
              class="pa-0 ma-0"
              style="width: 100%; height: 100%; border-radius: 0%"
            >
              <v-img src="https://iblaos.com/iblaos/image/logo.svg" />
            </v-btn>
          </v-col>
          <v-col cols="8" class="px-0">
            <v-col style="width: 100%; height: 140px" class="color_background">
              <v-row
                style="width: 100%; height: 100%"
                class="color_background"
                outlined
              >
                <v-col
                  cols="2"
                  class="color_background pa-0"
                  style="width: 100%; height: 100%"
                >
                  <v-btn
                    class="color_background"
                    @mouseenter="showText = 't'"
                    text
                    style="width: 100%; height: 100%; border-radius: 0%"
                  >
                    s
                  </v-btn>
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
        style="top: 100px; position: fixed; z-index: 100"
      >
        <v-card-text @mouseleave="showText = 'n'" class="pa-0">
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
      </v-col>
      <Nuxt />
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
