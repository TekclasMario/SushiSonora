<template>
  <div id="rolls_section">
    <v-card height="657" class="black">
      <div id="rolls_title">
        <h1 class="text-xs-center rolls_anim">{{ $t("rolls") }}</h1>
      </div>
      <div id="rolls_card"></div>

      <div id="placemat_pic">
        <v-img src="/Rolls-imgs/placemat.png">
          <v-container id="rolls_menu">
            <v-flex>
              <v-layout justify-center row wrap>
                <v-card id="rolls_info" flat tile v-for="menu in rolls" :key="menu.text">
                  <h4 class="white--text text-xs-center pa-1">{{ menu.text }}</h4>
                  <p class="white--text">{{ menu.info }}</p>
                  <p class="white--text">{{ menu.price }}</p>
                </v-card>
              </v-layout>
              <v-layout justify-center>
                <v-card
                  color="black"
                  class="mt-3 pa-1"
                  width="37.9rem"
                  v-for="menu in platter"
                  :key="menu.text"
                >
                  <h4 class="white--text text-xs-center pa-1 mt-1">{{ menu.text }}</h4>
                  <p class="white--text text-xs-center">{{ menu.info }}</p>
                  <p class="white--text text-xs-center">{{ menu.price }}</p>
                </v-card>
              </v-layout>
            </v-flex>
          </v-container>
        </v-img>
      </div>
      <div id="caterpillar_pic">
        <v-img class="cat_anim" src="/Rolls-imgs/caterpiller.png"></v-img>
      </div>
    </v-card>
  </div>
</template>

<style scoped>
#rolls_section {
  position: relative;
}

#rolls_title {
  height: 10rem;
  margin-top: 10rem;
}

#rolls_card {
  background-color: #57524c4c;
  position: absolute;
  height: 506px;
  width: 862px;
  margin-left: 30rem;
}

#caterpillar_pic {
  position: absolute;
  height: 303.4px;
  width: 356.03px;
  margin-top: 7rem;
  margin-left: 10rem;
}

#placemat_pic {
  position: absolute;
  height: 358px;
  width: 737px;
  margin-top: 2.9rem;
  margin-left: 38rem;
}

#rolls_img_container {
  margin-top: 2rem;
  margin-left: 13.5rem;
  width: 34rem;
}

.rolls_anim {
  color: grey;
  transition: color 0.9s ease-out !important;
}

#rolls_img {
  margin-bottom: 2rem;
  border-radius: 166px;
  width: 103.45px;
  height: 63.93px;
  transform: rotate(-90deg);
}

#rolls_menu {
  margin-top: 2rem;
  margin-left: 10rem;
  width: 45rem;
  padding: 0;
}

#rolls_info {
  margin-left: 0.5rem;
  margin-top: 0.5rem;
  font-size: 0.64rem;
  font-weight: lighter;
  text-align: center;
  text-indent: 0.37rem;
  background-color: black;
  width: 125px;
  height: 120px;
  padding: 0.5rem;
}

.cat_anim:hover {
  animation-name: zoomOutUp;
  animation-duration: 2s;
}

@media screen and (max-width: 1288px) {
  #caterpillar_pic,
  #rolls_card {
    display: none;
  }

  #placemat_pic {
    margin-left: 0rem;
    width: 100%;
  }
  #rolls_menu {
    margin-top: 8rem;
    margin-left: 25rem;
    width: 45rem;
    padding: 1rem;
  }
}

@media screen and (max-width: 931px) {
  #rolls_menu {
    width: 100%;
    margin: 1.5rem 0rem 0rem 0.5rem !important;
  }
}

@media screen and (max-width: 732px) {
  #placemat_pic {
    width: 100%;
  }

  #rolls_menu {
    width: 100%;
    margin: 0rem 0rem 0rem 1.5rem !important;
  }
}

@media screen and (max-width: 531px) {
  #placemat_pic {
    transform: rotate(90deg);
    margin-top: 0;
    margin-left: 1.8rem;
    width: 40rem;
  }

  #rolls_menu,
  #rolls_card {
    width: 35rem;
    margin: 0rem 0rem 0rem 2.5rem !important;
    transform: rotate(-90deg);
    /* width: 50%; */
  }
}

@media screen and (max-width: 484px) {
  #placemat_pic {
    margin-top: 0;
    margin-left: 1.8rem;
    width: 30rem;
  }

  #rolls_info {
    margin-left: 0.5rem;
    margin-top: 0.5rem;
    font-size: 0.3rem;
    font-weight: lighter;
    text-align: center;
    text-indent: 0.37rem;
    background-color: black;
    width: 55px;
    height: 80px;
    padding: 0.5rem;
  }

  #rolls_menu,
  #rolls_card {
    width: 30rem;
    padding: 2rem;
    margin: 0rem 0rem 0rem 0rem !important;
  }
}

@media screen and (max-width: 414px) {
  #placemat_pic {
    margin-top: 0rem;
    margin-right: 0rem;
    margin-left: 0rem;
    margin-bottom: 0rem;
    width: fill;
  }

  #rolls_info {
    margin-left: 0.5rem;
    margin-top: 0.5rem;
    font-size: 0.7rem;
    font-weight: lighter;
    text-align: center;
    text-indent: 0.37rem;
    background-color: black;
    width: 100px;
    height: 100px;
    padding: 0rem;
  }

  #rolls_menu,
  #rolls_card {
    width: 30.5rem;
    padding: 0rem;
    margin: 0rem 0rem 0rem 0.9rem !important;
  }
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
    platter() {
      return [
        {
          text: this.$t("sushitray"),
          info: this.$t("sushitrayinfo"),
          price: this.$t("sushitrayprice")
        }
      ];
    },
    rolls() {
      return [
        {
          text: this.$t("sushisonora"),
          info: this.$t("sushilessinfo"),
          price: this.$t("sushilessprice")
        },
        {
          text: this.$t("sushidog"),
          info: this.$t("sushidoginfo"),
          price: this.$t("sushidogprice")
        },
        {
          text: this.$t("extremeroll"),
          info: this.$t("extremeinfo"),
          price: this.$t("extremeprice")
        },
        {
          text: this.$t("vegasroll"),
          info: this.$t("vegasinfo"),
          price: this.$t("vegasprice")
        },
        {
          text: this.$t("cronchiroll"),
          info: this.$t("cronchiinfo"),
          price: this.$t("cronchiprice")
        },
        {
          text: this.$t("spicytuna"),
          info: this.$t("spicyinfo"),
          price: this.$t("spicyprice")
        },
        {
          text: this.$t("sushinola"),
          info: this.$t("sushininfo"),
          price: this.$t("sushinprice")
        },
        {
          text: this.$t("shrimptempura"),
          info: this.$t("shrimpteminfo"),
          price: this.$t("shrimptemprice")
        }
      ];
    }
  }
};
</script>