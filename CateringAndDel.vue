<template>
  <v-card color="black">
    <h1 class="text-xs-center grey--text pa-5 rolls_anim">{{ $t("catering") }}</h1>
    <v-layout justify-center class="responsive" row>
      <v-card class="text-xs-center mr-5 black" v-for="option in options" :key="option.title">
        <img height="283" class="product_image" :src="option.image">
        <v-card-text class="grey--text">
          <div color="black" class="subheading">{{option.title}}</div>
        </v-card-text>
        <v-btn :icon="option.media" :href="option.link" target="_blank" class="mx-3">
          <v-icon :color="option.color" large class="pa-2 loc_anim" size="24px">{{ option.media }}</v-icon>
        </v-btn>
        <p class="grey--text">{{option.info}}</p>
      </v-card>
    </v-layout>
  </v-card>
</template>

<style scoped>
@media screen and (max-width: 824px) {
  .responsive {
    flex-direction: column;
  }
}

@media screen and (max-width: 540px) {
  .product_image {
    padding-left: 2rem;
    width: 100%;
  }
}
</style>


<script>
export default {
  data() {
    return {
      options: [
        {
          title: "We Do Catering! Call us Today",
          image: "/Delivery-imgs/catering.jpg",
          media: "fas fa-phone-square",
          color: "#006847",
          info: "602-278-9355",
          link: "tel:+602-278-9355"
        },
        {
          title: "Delivery",
          image: "/Delivery-imgs/nowongh.jpg",
          media: "fas fa-car",
          color: "#CE1126",
          info: "Grub Hub!",
          link:
            "https://www.grubhub.com/restaurant/sushi-sonora-sports-bar--restaurant-6544-w-thomas-rd-phoenix/1193156"
        }
      ]
    };
  }
};
</script>
