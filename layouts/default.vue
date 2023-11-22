<template>
  <div @mouseleave="showText = false">
    <v-app-bar
      flat
      app
      style="background-color: rgb(102, 48, 143)"
      height="100px"
    >
      <v-row>
        <v-col cols="4" style="background-color: ">
          <v-app-bar-title style="display: flex; align-items: flex-start">
            <!-- Title-->
            <div
              style="display: flex; align-items: flex-start; margin-right: auto"
            >
              <v-img
                src="https://iblaos.com/iblaos/image/logo.svg"
                aspect-ratio="1.777"
                contain
                style="max-width: 300px; height: 150px; margin-top: 0"
              ></v-img>
            </div>
          </v-app-bar-title>
        </v-col>
        <v-col cols="8" class="blue">
          <v-col
            v-if="true"
            style="
              display: flex;
              align-items: center;
              justify-content: center;
              height: 100%;
            "
          >
            <!-- Left side content -->
            <div
              style="
                height: 100%;
                display: flex;
                align-items: center;
                justify-content: center;
              "
            >
              <div>
                <v-btn
                  class="about-btn"
                  style="height: 100px; color: transparent"
                  text
                  @mouseenter="showText = 'About'"
                >
                  <div class="wrapper">
                    <div style="padding-bottom: 10px; color: white" fontsize>
                      About
                    </div>
                    <div style="color: #aca8a8; text-transform: uppercase">
                      i<span style="text-transform: lowercase"
                        >ndoChina
                        <span style="text-transform: uppercase">B</span
                        >ank</span
                      >
                    </div>
                  </div>
                </v-btn>
                <v-btn
                  class="about-btn"
                  style="
                    height: 100px;
                    color: transparent;
                    box-shadow: none;
                    border: none;
                  "
                  text
                  @mouseenter="showText = 'Personal'"
                >
                  <div class="wrapper">
                    <div style="padding-bottom: 10px; color: white" fontsize>
                      personal
                    </div>
                    <div style="color: #aca8a8; text-transform: uppercase">
                      b<span style="text-transform: lowercase">anking </span>
                    </div>
                  </div>
                </v-btn>
                <v-btn
                  class="about-btn"
                  style="
                    height: 100px;
                    color: transparent;
                    box-shadow: none;
                    border: none;
                  "
                  text
                  @mouseenter="showText = 'Corporate'"
                >
                  <div class="wrapper">
                    <div style="padding-bottom: 10px; color: white" fontsize>
                      corporate
                    </div>
                    <div style="color: #aca8a8; text-transform: uppercase">
                      b<span style="text-transform: lowercase">anking </span>
                    </div>
                  </div>
                </v-btn>
                <v-btn
                  class="about-btn"
                  style="
                    height: 100px;
                    color: transparent;
                    box-shadow: none;
                    border: none;
                  "
                  text
                  @mouseenter="showText = 'Premier'"
                >
                  <div class="wrapper">
                    <div style="padding-bottom: 10px; color: white" fontsize>
                      premier
                    </div>
                    <div style="color: #aca8a8; text-transform: uppercase">
                      b<span style="text-transform: lowercase">anking </span>
                    </div>
                  </div>
                </v-btn>
              </div>

              <v-btn
                @mouseenter="showText = false"
                class="about-btn"
                style="height: 100px; color: white"
                text
              >
                <div class="wrapper">
                  <div style="padding-bottom: 10px" fontsize>reward</div>
                  <div style="color: #aca8a8; text-transform: uppercase">
                    P<span style="text-transform: lowercase">rogram</span>
                  </div>
                </div>
              </v-btn>
              <div>
                <v-btn
                  class="about-btn"
                  style="height: 100px; color: white"
                  text
                >
                  <div class="wrapper">
                    <div style="padding-bottom: 10px" fontsize>cool</div>
                    <div style="color: #aca8a8; text-transform: uppercase">
                      L<span style="text-transform: lowercase">ifestyle </span>
                    </div>
                  </div>
                </v-btn>
              </div>
            </div>
          </v-col>
          <v-col
            v-else
            style="
              display: flex;
              align-items: center;
              justify-content: flex-end;
              height: 100%;
            "
          >
            <!-- Left side content -->
            <div
              style="
                height: 100%;
                display: flex;
                align-items: center;
                justify-content: flex-end;
              "
            >
              gg
            </div>
          </v-col>
        </v-col>
        <!-- Right side content -->
      </v-row>
    </v-app-bar>

    <div disabled="true">
      <v-card flat class="red-background" height="95px">
        <v-main>
          <v-col
            v-if="
              showText == 'About' ||
              showText == 'Personal' ||
              showText == 'Corporate' ||
              showText == 'Premier'
            "
            class="pa-0"
            style="top: 80px; position: fixed; z-index: 10"
          >
            <div class="pa-0">
              <v-col class="pa-0">
                <v-row>
                  <v-col
                    cols="12"
                    class="pa-0"
                    style="height: 1px; width: 100%"
                  >
                    <v-row>
                      <v-col cols="4"> </v-col>
                      <v-col cols="8">
                        <v-row>
                          <v-col cols="2" disabled="true">
                            <v-icon
                              size="50"
                              color="rgb(255, 128, 0)"
                              style="
                                bottom: 35px;
                                width: 50px;
                                margin-left: 200px;
                              "
                              v-if="showText == 'About'"
                              >mdi-triangle-small-up</v-icon
                            >
                          </v-col>
                          <v-col cols="2">
                            <v-icon
                              size="50"
                              color="rgb(255, 128, 0)"
                              style="
                                bottom: 35px;
                                width: 50px;
                                margin-left: 160px;
                              "
                              v-if="showText == 'Personal'"
                              >mdi-triangle-small-up</v-icon
                            >
                          </v-col>
                          <v-col cols="2">
                            <v-icon
                              size="50"
                              color="rgb(255, 128, 0)"
                              style="
                                bottom: 35px;
                                width: 50px;
                                margin-left: 120px;
                              "
                              v-if="showText == 'Corporate'"
                              >mdi-triangle-small-up</v-icon
                            >
                          </v-col>
                          <v-col cols="2">
                            <v-icon
                              size="50"
                              color="rgb(255, 128, 0)"
                              style="
                                bottom: 35px;
                                width: 50px;
                                margin-left: 60px;
                              "
                              v-if="showText == 'Premier'"
                              >mdi-triangle-small-up</v-icon
                            >
                          </v-col>
                        </v-row>
                      </v-col>
                    </v-row>
                  </v-col>
                </v-row>
              </v-col>
            </div>
          </v-col>
          <v-card>
            <Nuxt />
          </v-card>
          </v-main>
      </v-card>

      <div v-if="showText !== false">
        <div>
          <v-card
            @mouseenter="showText = 'About'"
            class="green-background"
            flat
            style="position: relative"
          >
          </v-card>
          <v-card
            @mouseenter="showText = 'About'"
            class="white-background"
            style="position: relative; z-index: -1"
          >
            <v-card-text class="red" @mouseenter="showText = 'About'">
              <v-container>
                <v-card-text> ff </v-card-text>
              </v-container>
            </v-card-text>
          </v-card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showText: false,
    };
  },
};
</script>


<style scoped>
.color_background {
  background-color: rgb(102, 48, 143);
  color: #fff;
}
.about-btn:hover {
  background-color: #662483;
}
.wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.red-background {
  width: 100%;
  height: 13vh;
  border-radius: 0%;
}

.green-background {
  background-color: rgb(255, 128, 0);
  width: 100%;
  height: 1.5vh;
  z-index: 100;
  border-bottom-right-radius: 0%;
  border-bottom-left-radius: 0%;
}
</style>









