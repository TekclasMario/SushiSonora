<template>
  <v-flex align-self-center>
    <v-img id="main_cover_img" src="cover5.png">
 
        <v-layout align-end id="banner_text">
          <v-flex text-xs-right>
            <h3 class="white--text animated bounceInLeft slower">{{ $t("welcomeMsg") }}</h3>
            <LangBtn/>
          </v-flex>
        </v-layout>
    
    </v-img>
    
     <v-layout align-end id="banner_text2">
          <v-flex text-xs-right>
            <h3 class="white--text animated bounceInLeft slower">{{ $t("welcomeMsg") }}</h3>
            <LangBtn/>
          </v-flex>
	</v-layout>
    
    
  </v-flex>
</template>

<script>
import LangBtn from "@/components/LangBtn";

export default {
  name: "App",
  components: {
    LangBtn
  },
  data() {
    return {
      //
    };
  }
};
</script>




