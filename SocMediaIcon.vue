   <template>
  <div>
    <v-container>
      <div class="ma-5">
        <h1 class="text-xs-center grey--text rolls_anim pr-5">{{ $t("followuson") }}</h1>
      </div>
      <div class="text-xs-center">
        <v-btn
          v-for="icon in icons"
          target="_blank"
          :key="icon.media"
          :icon="icon.media"
          :href="icon.link"
          class="mx-3"
          dark
        >
          <v-icon :color="icon.color" large class="socmed pa-2 animated">{{icon.media}}</v-icon>
        </v-btn>
      </div>
    </v-container>
  </div>
</template>

  <script>
export default {
  data: () => ({
    icons: [
      {
        media: "fab fa-facebook",
        color: "#006847",
        link: "https://www.facebook.com/SushiSonora/?tn-str=k*F"
      },

      {
        media: "fab fa-instagram",
        color: "#CE1126",
        link: "https://www.instagram.com/sushisonora/"
      }
    ]
  })
};
</script>