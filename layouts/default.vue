<!--<template>
  <v-app dark>
    <v-app-bar app class="red" style="background-color: rgb(102, 48, 143);">
      <v-row flat fluid align="center" justify="center" class="absolute-fill" style="background-color: rgb(102, 48, 143); margin: 0; padding: 0;">
        <v-col cols="4" class="text-center align-center pt-8" style="padding-right: 150px; height: 150px;">
          <v-img
            src="https://iblaos.com/iblaos/image/logo.svg"
            aspect-ratio="1.777"
            contain
            style="margin-top: 10px; height: 100%; margin-right: 30px;"
          ></v-img>
        </v-col>
        <v-col cols="8" justify="center" align="center">
        </v-col>
      </v-row>
    </v-app-bar>
  </v-app>
</template> -->
<template>
  <div class="toolbar">
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
              <v-btn
                class="about-btn"
                style="height: 100px; color: transparent"
                text
                @mouseenter="showText = 'About'"
                @mouseleave="showText = false"
              >
                <div class="wrapper">
                  <div style="padding-bottom: 10px; color:white" fontsize>About</div>
                  <div style="color: #aca8a8; text-transform: uppercase">
                    i<span style="text-transform: lowercase"
                      >ndoChina
                      <span style="text-transform: uppercase">B</span>ank</span
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
                @mouseleave="showText = false"
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
                @mouseleave="showText = false"
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
                @mouseleave="showText = false"
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
              <v-btn class="about-btn" style="height: 100px; color: white" text>
                <div class="wrapper">
                  <div style="padding-bottom: 10px" fontsize>reward</div>
                  <div style="color: #aca8a8; text-transform: uppercase">
                    P<span style="text-transform: lowercase">rogram</span>
                  </div>
                </div>
              </v-btn>
              <v-btn class="about-btn" style="height: 100px; color: white" text>
                <div class="wrapper">
                  <div style="padding-bottom: 10px" fontsize>cool</div>
                  <div style="color: #aca8a8; text-transform: uppercase">
                    L<span style="text-transform: lowercase">ifestyle </span>
                  </div>
                </div>
              </v-btn>
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
    <!-- <v-row style="background-color:yellow">

      <v-divider color="yellow"></v-divider>
      </v-row> -->
    <div disabled="true">
      <v-card flat class="red-background" style="">
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
            <div
              @mouseenter="showText = 'About' || showText == 'Personal'"
              class="pa-0"
            >
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
                              v-if=" showText == 'About'"
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
          <!-- <Nuxt /> -->
        </v-main>
      </v-card>
      <v-card
        class="green-background"
        flat
        v-if="
          showText == 'About' ||
          showText == 'Personal' ||
          showText == 'Corporate' ||
          showText == 'Premier'
        "
        @mouseenter="showText = 'About'"
        @mouseleave="showText = false"
        style="position:relative;"
      >
      </v-card>
      <v-card
        class="white-background"
        
        v-if="
          showText == 'About' ||
          showText == 'Personal' ||
          showText == 'Corporate' ||
          showText == 'Premier'
        "
        @mouseenter="showText = 'About'"
        @mouseleave="showText = false"
        style="position: relative;z-index:-1;top:10px"

      >
        <v-card-text>
          <v-container>
            <v-row>
              <v-col> hhhhhh </v-col>
            </v-row>
          </v-container>
        </v-card-text>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showText: "",
    };
  },
};
</script>


<style scoped>
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









<!--
<style scoped>
.v-container {
  max-width: 60% !important;
}
</style>
-->
