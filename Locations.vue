<template>
  <v-card color="black">
    <v-layout justify-center>
      <v-card
        class="text-xs-center mr-2 mb-4 mt-5 black"
        v-for="location in locations"
        :key="location.title"
        height="350"
        width="350"
      >
        <v-img width="100%" height="195.74px" :src="location.image"></v-img>
        <v-card-text class="black grey--text">
          <div>{{location.title}}</div>
          <div>{{location.phone}}</div>
          <div>{{location.address}}</div>
        </v-card-text>

        <v-btn :icon="location.map" :href="location.link" target="_blank" class="mx-3 loc_anim">
          <v-icon :color="location.color" large class="pa-2" size="24px">{{ location.map }}</v-icon>
        </v-btn>
      </v-card>
    </v-layout>
  </v-card>
</template>


<script>
export default {
  data() {
    return {
      locations: [
        {
          title: "Sushi Sonora #1",
          image: "/Locations-img/location1.jpg",
          phone: "602-278-9355",
          address: "355 W MacDowel Rd. Phoenix, AZ 85009",
          map: "fas fa-map",
          color: "#006847",
          link:
            "https://www.google.com/maps/place/Sushi+Sonora/@33.465664,-112.1150739,13z/data=!4m8!1m2!2m1!1ssushi+sonora+!3m4!1s0x0:0x84537a2e0bcc89b4!8m2!3d33.4657093!4d-112.1367538"
        },
        {
          title: "Sushi Sonora #2",
          image: "/Locations-img/location2.jpg",
          phone: "602-267-1697",
          address: "1400 N 32th St. Phoenix, AZ 85008",
          map: "fas fa-map-pin",
          color: "#f2f2f2",
          link:
            "https://www.google.com/maps/place/Sushi+Sonora/@33.4667696,-112.026224,14.25z/data=!4m8!1m2!2m1!1ssushi+sonora+!3m4!1s0x0:0x1f87218055d42da6!8m2!3d33.4640222!4d-112.0131361"
        },
        {
          title: "Sushi Sonora #3",
          image: "/Locations-img/location3.jpg",
          phone: "602-466-6436",
          address: "6544 W Thomas St. Phoenix, AZ 85033",
          map: "fas fa-map",
          color: "#CE1126",
          link:
            "https://www.google.com/maps/place/Sushi+Sonora+Sports+Bar+%26+Restaurant/@33.428334,-112.0756933,11.16z/data=!4m8!1m2!2m1!1ssushi+sonora!3m4!1s0x0:0x3687b7df76c31ab2!8m2!3d33.4814244!4d-112.201395"
        }
      ]
    };
  }
};
</script>