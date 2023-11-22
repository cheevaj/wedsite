<template>
  <div>
    <v-window v-model="onboarding" reverse>
      <v-window-item v-for="item in image" :key="`card-${item}`">
        <v-card
          @mouseenter="stopAutoSlide"
          @mouseleave="startAutoSlide"
          color="grey"
          height="100%"
        >
          <v-row class="fill-height" align="center" justify="center">
            <v-img style="height: 100%" :src="item">
              <v-card-actions
                style="height: 100%"
                class="justify-space-between"
              >
                <v-btn @mouseenter="colorIcon" @mouseleave="colorIcon"  style="height: 100%; width: 15%;background-color: transparent;
                        box-shadow: none;
                        border: none;
                        color:transparent;" text @click="next">
                  <v-icon :color="colors" size="55"
                    >mdi-chevron-left</v-icon
                  >
                </v-btn>
                <v-item-group
                  style="height: 100%"
                  v-model="onboarding"
                  mandatory
                >
                  <v-item
                    style="top: 90%"
                    v-for="item in image"
                    :key="`card-${item}`"
                    v-slot="{ active, toggle }"
                  >
                    <v-btn
                      class="mx-1"
                      :input-value="active"
                      icon
                      @click="toggle"
                      style="
                        background-color: transparent;
                        box-shadow: none;
                        border: none;
                        color:transparent;
                      "
                    >
                      <v-icon size="55">mdi-minus</v-icon>
                    </v-btn>
                  </v-item>
                </v-item-group>
                <v-btn @mouseenter="colorIcon" @mouseleave="colorIcon"
                  style="height: 100%; width: 15%"
                  text
                  @click="prev(item)"
                >
                  <v-icon size="55" :color="colors"
                    >mdi-chevron-right</v-icon
                  >
                </v-btn>
              </v-card-actions>
            </v-img>
          </v-row>
        </v-card>
      </v-window-item>
    </v-window>
    <v-row>
      <v-col cols="4" class=""></v-col>
      <v-card-text v-if="false" class="red text-center"> fff </v-card-text>
      <v-card-text v-else class="red text-right"> ggg </v-card-text>
    </v-row>
  </div>
</template>
<script>
export default {
  data: () => ({
    onboarding: 0,
    colors:"#e5e5e5",
    image: [
      "https://iblaos.com/iblaos/image/slide/20230912154356_2.jpg",
      "https://iblaos.com/iblaos/image/slide/20230913144236_2.jpg",
      "https://iblaos.com/iblaos/image/slide/20230913145105_2.jpg",
    ],
  }),
  computed: {
    length() {
      return this.image.length;
    },
  },
  methods: {
    next() {
      this.onboarding =
        this.onboarding + 1 === this.length ? 0 : this.onboarding + 1;
    },
    prev() {
      this.onboarding =
        this.onboarding - 1 < 0 ? this.length - 1 : this.onboarding - 1;
    },
    startAutoSlide() {
      this.autoSlideInterval = setInterval(() => {
        this.prev();
      }, 7500); // Slide every 4 seconds (4000 milliseconds)

      // No need to reset this.manualSlide here
    },
    stopAutoSlide() {
      clearInterval(this.autoSlideInterval);
    },
    colorIcon(){
      if (this.colors!="#ffffff"){
        this.colors="#ffffff";
      }
      else {
        this.colors="#e5e5e5";
      }
    },
  },
  mounted() {
    // Start automatic image slide when the component is mounted
    this.startAutoSlide();
  },
};
</script>

