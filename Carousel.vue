<template>
  <div>
    <v-container>
      <h1 class="text-xs-center grey--text rolls_anim pb-5">{{ $t("socialmedia") }}</h1>
      <v-carousel hide-delimiters id="carousel-items">
        <v-carousel-item
          v-for="(item,i) in items"
          :key="i"
          reverse-transition="fade"
          transition="fade"
        >
          <img :src="item.src" style="width:100%">
        </v-carousel-item>
      </v-carousel>
    </v-container>
  </div>
</template>

<style scoped lang="stylus">
#carousel {
  margin-bottom: 0rem;
}

#example-custom-transition {
  .fade {
    &-enter-active, &-leave-active, &-leave-to {
      transition: 0.3s ease-out;
      position: absolute;
      top: 0;
      left: 0;
    }

    &-enter, &-leave, &-leave-to {
      opacity: 0;
    }
  }
}

@media screen and (max-width: 889px) {
  #carousel-items {
    height: 200px !important;
  }
}
</style> 




<script>
export default {
  data() {
    return {
      items: [
        {
          src: "/Reviews/reviewsfb.png"
        },
        {
          src: "/Reviews/reviewsfb2.png"
        },
        {
          src: "/Reviews/reviewsfb3.png"
        },
        {
          src: "/Reviews/reviewsfb4.png"
        }
      ]
    };
  }
};
</script> 

