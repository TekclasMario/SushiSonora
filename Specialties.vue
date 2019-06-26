<template>
  <div id="specialties_section">
    <v-container pa-0>
      s
      <v-img id="cover_img" class="specialties_img" src="/Specialty-imgs/newcover.png"></v-img>
      <v-sheet color="black" id="menu_card">
        <h1 class="pb-3 specialties_anim">{{ $t("specialties") }}</h1>

        <v-container fluid>
          <v-layout justify-center row wrap>
            <v-card
              class="menu_items"
              color="black"
              width="152px"
              height="100%"
              flat
              tile
              v-for="menu in food"
              :key="menu.image"
            >
              <v-img class="menu_items_anim" width="152px" height="95.74px" :src="menu.image"></v-img>
              <v-card-text class="black menu_text">
                <h3 class="text-xs-center">{{ menu.text }}</h3>
                <p id="menu_info">{{ menu.info }}</p>
                <p class="menu_info_price">{{ menu.price }}</p>
              </v-card-text>
            </v-card>
          </v-layout>
        </v-container>
      </v-sheet>
    </v-container>
  </div>
</template>

<style scoped>
#specialties_section {
  height: 1200px !important;
  position: relative !important;
}

#menu_card {
  position: absolute;
  margin-top: 6rem !important;
  margin-left: 40.9rem;
  background-color: #57524c4c;
  width: 665px;
}

#menu_info {
  font-size: 0.84rem;
  font-weight: lighter;
  text-align: center;
  text-indent: 0.67rem;
  color: white;
}

.menu_info_price {
  font-size: 0.84rem;
  font-weight: lighter;
  text-align: center;
  text-indent: 0.67rem;
  color: white;
  transition: all 0.5s ease-out !important;
}

.menu_info_price:hover {
  color: #cbf442;
  animation-name: heartBeat;
  animation-duration: 5s;
  font-size: 1.5rem;
}

#cover_img {
  position: absolute;
  width: 456.84px;
  height: 1063.74px;
}

.menu_items_anim:hover {
  animation-name: rubberBand;
  animation-duration: 2s;
}

.menu_text {
  color: red;
  transition: color 0.9s ease-out !important;
}

.rolls_anim:hover,
.specialties_anim:hover,
.menu_text:hover {
  color: #cbf442;
}

.specialties_anim {
  animation-name: fadeInRightBig;
  animation-duration: 3s;
  animation-delay: 6s;
  animation-fill-mode: both;
  color: grey;
  transition: color 0.9s ease-out !important;
}

.specialties_img {
  animation-name: fadeInLeftBig;
  animation-duration: 3s;
  animation-delay: 5s;
  animation-fill-mode: both;
}

@media screen and (max-width: 1288px) {
  #specialties_section {
    height: 1000px !important;
  }

  .specialties_anim,
  .specialties_img {
    display: none;
    animation: none;
  }
  #menu_card {
    position: absolute;
    margin-top: 0rem !important;
    margin-left: 0rem;
    background-color: #57524c4c;
    width: 95%;
  }
}

@media screen and (max-width: 776px) {
  #specialties_section {
    height: 2300px !important;
  }
  .specialties_anim,
  .specialties_img {
    display: none;
    animation: none;
  }

  #menu_card {
    position: absolute;
    margin-top: 0rem !important;
    margin-left: 0rem;
    background-color: #57524c4c;
    width: 100%;
  }
}

@media screen and (max-width: 443px) {
  /* #about_img {
    width: 400px !important;
    height: 400px !important;
    margin-top: 5rem;
  } */
}

@media screen and (max-width: 400px) {
  /* #about_img {
    width: 100% !important;
    height: 300px !important;
    margin-top: 5rem;
  } */
}
</style>




<script>
import i18n from "@/plugins/i18n";
export default {
  data() {
    return {
      item: []
    };
  },

  computed: {
    food() {
      return [
        {
          image: "/Specialty-imgs/bomba.png",
          text: this.$t("bomba"),
          info: this.$t("bombainfo"),
          price: this.$t("bombaprice")
        },
        {
          image: "/Specialty-imgs/percheronroll.png",
          text: this.$t("percheronroll"),
          info: this.$t("percherinfo"),
          price: this.$t("percherprice")
        },
        {
          image: "/Specialty-imgs/polansroll.png",
          text: this.$t("polansroll"),
          info: this.$t("polandinfo"),
          price: this.$t("polandprice")
        },
        {
          image: "/Specialty-imgs/dinamita-roll.png",
          text: this.$t("dinamita"),
          info: this.$t("dinamitainfo"),
          price: this.$t("dinamitaprice")
        },
        {
          image: "/Specialty-imgs/shushiless.png",
          text: this.$t("sushiless"),
          info: this.$t("sushilessinfo"),
          price: this.$t("sushilessprice")
        },
        {
          image: "/Specialty-imgs/teriyaki.png",
          text: this.$t("teriyaki"),
          info: this.$t("teriyakiinfo"),
          price: this.$t("teriyakiprice")
        },
        {
          image: "/Specialty-imgs/kono.png",
          text: this.$t("kono"),
          info: this.$t("konoinfo"),
          price: this.$t("konoprice")
        },
        {
          image: "/Specialty-imgs/kushiagui.png",
          text: this.$t("kushiagui"),
          info: this.$t("kushiinfo"),
          price: this.$t("kushiprice")
        },
        {
          image: "/Specialty-imgs/yakimeshi.png",
          text: this.$t("yakimeshi"),
          info: this.$t("yakiinfo"),
          price: this.$t("yakiiprice")
        },
        {
          image: "/Specialty-imgs/noname.png",
          text: this.$t("cielomartierra"),
          info: this.$t("cielinfo"),
          price: this.$t("cieliprice")
        },
        {
          image: "/Specialty-imgs/subarachi.png",
          text: this.$t("subarachi"),
          info: this.$t("dinamitainfo"),
          price: this.$t("dinamitaprice")
        },
        {
          image: "/Specialty-imgs/orangechik.png",
          text: this.$t("orangechik"),
          info: this.$t("orangeinfo"),
          price: this.$t("orangeprice")
        },
        {
          image: "/Specialty-imgs/yakishoba.png",
          text: this.$t("yakishoba"),
          info: this.$t("yakishobainfo"),
          price: this.$t("yakishobaprice")
        },
        {
          image: "/Specialty-imgs/guamuchilito.png",
          text: this.$t("guamuchilito"),
          info: this.$t("guamuinfo"),
          price: this.$t("guamuprice")
        },
        {
          image: "/Specialty-imgs/elrey.png",
          text: this.$t("elrey"),
          info: this.$t("elreyinfo"),
          price: this.$t("elreyprice")
        },
        {
          image: "/Specialty-imgs/cordonblue.png",
          text: this.$t("cordonblue"),
          info: this.$t("cordonblueinfo"),
          price: this.$t("cordonblueprice")
        }
      ];
    }
  }
};
</script>
