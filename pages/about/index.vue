<template>
  <div>
      <v-img src="https://iblaos.com/iblaos/image/about/20220802164610_2.jpg" />
      <div style="display: flex; right: 90%; top: ;">
        <v-btn text fab x-small @click="show = !show" color="transparent">
          <v-icon v-if="show" style="color: #8e44ad" size="35">mdi-cached</v-icon>
          <v-icon v-else style="color: #8e44ad" size="35">mdi-sync</v-icon>
        </v-btn>
      </div>
    <v-card-text v-if="show">
      <v-card-text>
        <v-row align="center" justify="center">
          <v-card
            min-height="250px"
            width="200px"
            class="text-center my-1 mx-2"
          >
            <v-card flat height="200px" width="200px">
              <v-img
                style="height: 100%; width: 100%"
                src="https://iblaos.com/iblaos/image/about/20211129163935_2.JPG"
              />
            </v-card>
            <v-card-text class="pa-0" style="color: #662483"
              >Mrs. Thavone Vongsombath</v-card-text
            >
            <v-card-text class="pa-0" style="color: #8e44ad">
              Chairperson</v-card-text
            >
          </v-card>
        </v-row>
      </v-card-text>
      <v-card-text>
        <v-row align="center" justify="center">
          <v-card
            min-height="250px"
            width="200px"
            class="text-center my-1 mx-2"
          >
            <v-card flat height="200px" width="200px">
              <v-img
                style="height: 100%; width: 100%"
                src="https://iblaos.com/iblaos/image/about/20211129164254_2.JPG"
              />
            </v-card>
            <v-card-text class="pa-0" style="color: #662483"
              >Mr. Jang Woojin</v-card-text
            >
            <v-card-text class="pa-0" style="color: #8e44ad">
              Vice Chairman</v-card-text
            >
          </v-card>
        </v-row>
      </v-card-text>
      <v-card-text>
        <v-row align="center" justify="center">
          <v-card
            min-height="250px"
            width="200px"
            class="text-center my-1 mx-2"
          >
            <v-card flat height="200px" width="200px">
              <v-img
                style="height: 100%; width: 100%"
                src="https://iblaos.com/iblaos/image/about/20211129164234_2.JPG"
              />
              <v-card-text class="pa-0" style="color: #662483"
                >Mr. Bounheng SOUPHIDA</v-card-text
              >
              <v-card-text class="pa-0" style="color: #8e44ad">
                Vice Chairman</v-card-text
              >
            </v-card>
          </v-card>
        </v-row>
      </v-card-text>
      <v-card-text>
        <v-row align="center" justify="center">
          <v-card
            min-height="250px"
            width="200px"
            class="text-center my-1 mx-2"
            v-for="i in 4"
            :key="i"
            cols="2"
          >
            <v-card flat height="200px" width="200px">
              <v-img
                style="height: 100%; width: 100%"
                src="https://iblaos.com/iblaos/image/about/20211129164234_2.JPG"
              />
            </v-card>
            <v-card-text class="pa-0" style="color: #662483"
              >Mr. Bounheng SOUPHIDA</v-card-text
            >
            <v-card-text class="pa-0" style="color: #8e44ad">
              Vice Chairman</v-card-text
            >
          </v-card>
        </v-row>
      </v-card-text>
      <v-card-text>
        <v-row align="center" justify="center">
          <v-card
            min-height="250px"
            width="200px"
            class="text-center my-1 mx-2"
            v-for="i in 12"
            :key="i"
            cols="2"
          >
            <v-card flat height="200px" width="200px">
              <v-img
                style="height: 100%; width: 100%"
                src="https://iblaos.com/iblaos/image/about/20211129164234_2.JPG"
              />
            </v-card>
            <v-card-text class="pa-0" style="color: #662483"
              >Mr. Bounheng SOUPHIDA</v-card-text
            >
            <v-card-text class="pa-0" style="color: #8e44ad">
              Member</v-card-text
            >
          </v-card>
        </v-row>
      </v-card-text>
    </v-card-text>
    <v-card-text v-else align="center" justify="center" >
      <v-card flat width="1000px">
        <v-img
          src="https://www.bol.gov.la/en/fileupload/21-03-2019_1553151565.jpg"
        />
      </v-card>
    </v-card-text>
  </div>
</template>
<script>
export default {
  data() {
    return {
      show: true,
    };
  },
};
</script>