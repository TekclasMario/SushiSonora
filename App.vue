<template>
  <v-app class="black">
    <HelloWorld/>
    <AboutSection/>
    <Specialties/>
    <Rolls/>
    <Promotions/>
    <Carousel/>
    <Locations/>
    <CateringAndDel/>
    <SocMediaIcon/>
    <TekcalsFooter/>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import LangBtn from "@/components/LangBtn";
import AboutSection from "@/components/AboutSection";
import Specialties from "@/components/Specialties";
import Rolls from "@/components/Rolls";
import Promotions from "@/components/Promotions";
import Carousel from "@/components/Carousel";
import Locations from "@/components/Locations";
import CateringAndDel from "@/components/CateringAndDel";
import TekclasFooter from "@/components/TekclasFooter";
import SocMediaIcon from "@/components/SocMediaIcon";
import i18n from "@/plugins/i18n";
export default {
  name: "App",
  components: {
    HelloWorld,
    AboutSection,
    Specialties,
    Rolls,
    Promotions,
    Carousel,
    Locations,
    CateringAndDel,
    TekclasFooter,
    SocMediaIcon,
    LangBtn
  },
  data() {
    return {
      //
    };
  }
};
</script>

<style>
a {
  text-decoration: none;
  color: blue;
}
a:hover {
  color: red;
}

h1,
h3,
p {
  font-family: "Barlow", sans-serif;
}
/* Banner Section */

#main_cover_img {
  width: 777px !important;
  height: 777px !important;
  margin-top: 5rem;
}

#banner_text {
  height: 30rem;
  padding-top: 55rem;
  font-size: 1.4rem;
}

#banner_text2 {
  display: none;
}

/* About Section */

/* #about_container{
  padding: 20rem 0rem 0rem 0rem !important;
} */

/* #about_img {
  background-image: url("~/plate.png");
  width: 1462px !important;
  height: 1404px !important;
}

#about_card {
  margin-top: 6rem !important;
  margin-left: 4.9rem;
  background-color: #57524c4c;
  width: 685px;
  height: 345px;
}

#about_card2 {
  margin-top: 30rem !important;
  margin-left: 50.9rem;
  background-color: #57524c4c;
  width: 685px;
  height: 345px;
}

#about_txt {
  color: white;
  opacity: 100;
  font-family: "Barlow", sans-serif;
  font-size: 1.3rem;
  font-weight: lighter;
  text-indent: 50px;
  text-align: justify;
}
#about_txt2 {
  color: white;
  opacity: 100;
  font-family: "Barlow", sans-serif;
  font-size: 1.3rem;
  font-weight: lighter;
  text-indent: 50px;
  text-align: justify;
  padding: 6rem;
} */

/* specialties section */
/* 
#specialties_section {
  height: 1200px !important;
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
} */

/* Rolls section */
/* #rolls_title {
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
  margin-left: 14rem;
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
} */

/* Promotions */

/* #promotions {
  height: 1563.74px;
  padding: 24px;
} */

/* Social Media */

.socmed {
  animation-name: flip;
  animation-duration: 4s;
  animation-iteration-count: infinite;
}

/* Locations */

.loc_anim:hover {
  animation-name: jello;
  animation-duration: 1s;
  animation-iteration-count: infinite;
}

/*	Media Queries*/

@media screen and (max-width: 776px) {
  #main_cover_img {
    width: 444px !important;
    height: 444px !important;
    margin-top: 5rem;
  }

  #banner_text {
    display: none;
  }

  #banner_text2 {
    display: block;
  }
}

@media screen and (max-width: 443px) {
  #main_cover_img {
    width: 400px !important;
    height: 400px !important;
    margin-top: 5rem;
  }

  #banner_text {
    display: none;
  }
}

@media screen and (max-width: 400px) {
  #main_cover_img {
    width: 300px !important;
    height: 300px !important;
    margin-top: 5rem;
  }

  #banner_text {
    display: none;
  }
}
</style>