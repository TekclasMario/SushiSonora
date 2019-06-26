<template>
  <div id="promotions">
    <v-container>
      <v-layout class="ma-5 pa-5 promo">
        <v-container class="ma-5 pa-5 promo">
          <h1 class="text-xs-center grey--text rolls_anim">Specials and Events</h1>
          <v-img contain class="ma-5 pa-5 wood_img" src="/Promo-imgs/wooden-board-1.png">
            <v-layout column>
              <v-flex align-self-center>
                <v-img class="ma-3 img_cards" v-for="img in images" :src="img" :key="img.images"></v-img>
              </v-flex>
            </v-layout>
          </v-img>
        </v-container>
      </v-layout>
    </v-container>
  </div>
</template>

<style scoped>
#promotions {
  height: 1563.74px;
  padding: 24px;
}

.img_cards {
  width: 298px;
  height: 210px;
}

@media screen and (max-width: 889px) {
  #promotions {
    height: 1200.74px;
    padding: 0px;
  }
  .promo {
    margin: 0px !important;
    padding: 0px !important;
  }
}
@media screen and (max-width: 520px) {
  .wood_img {
    margin: 0px !important;
    padding: 0px !important;
  }
}
</style>

<script>
export default {
  data() {
    return {
      images: [
        "/Promo-imgs/ladiesnight.png",
        "/Promo-imgs/lunchspecial.png",
        "/Promo-imgs/promotions.png",
        "/Promo-imgs/rockenespanol.png"
      ]
    };
  }
};
</script>