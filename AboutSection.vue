<template>
  <v-card>
    <v-flex align-self-center>
      <v-img id="about_img" src="/plate.png">
        <v-sheet id="about_card">
          <div>
            <h1
              id="about_title"
              class="text-xs-center white--text animated fadeInDown fast delay-2s"
            >{{ $t("story") }}</h1>
            <h3
              id="about_txt"
              class="text-xs-center white--text animated flash slower delay-2s"
            >{{ $t("about") }}</h3>
          </div>
        </v-sheet>

        <v-sheet id="about_card2">
          <div>
            <p
              id="about_txt2"
              class="text-xs-center white--text animated rollIn slower delay-3s"
            >{{ $t("about2") }}</p>
          </div>
        </v-sheet>
      </v-img>
    </v-flex>
  </v-card>
</template>

<style scoped>
#about_img {
  /* position: relative; */
  /* background-image: url("~/plate.png"); */
  width: 100% !important;
  /*  height: 1404px !important; */
}

#about_card {
  /* position: absolute; */
  margin: 6rem 0rem 0rem 3.9rem !important;
  /* margin-left: 4.9rem; */
  background-color: #57524c4c;
  width: 685px;
  height: 345px;
}

#about_card2 {
  float: right;
  margin: 30rem 3.9rem 0rem 0rem;
  /* margin-left: 50.9rem; */
  background-color: #57524c4c;
  width: 685px;
  height: 345px;
}

#about_title {
  padding: 3rem;
  color: white;
  opacity: 100;
  font-family: "Barlow", sans-serif;
  font-size: 1.3rem;
  font-weight: lighter;
  text-indent: 50px;
  text-align: justify;
}

#about_txt {
  padding: 1rem 6rem 0rem 6rem;
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
}

@media screen and (max-width: 1395px) {
}

@media screen and (max-width: 776px) {
  #about_img {
    width: 100% !important;
    /* height: 100% !important; */
    margin-top: 0rem;
  }

  #about_card {
    margin: 0rem !important;
    padding-top: 10rem;
    background-color: #57524c4c;
    width: 100%;
    height: 50%;
  }

  #about_title {
    padding: 2rem 0 0 0.5rem;
    font-size: 1.3rem;
    font-weight: bold;
    text-indent: 50px;
    text-align: justify;
  }

  #about_txt {
    padding: 2rem;
    font-size: 0.9rem;
    text-indent: 20px;
    text-align: justify;
  }

  #about_card2 {
    margin: 0;
    background-color: #57524c4c;
    width: 100%;
    height: 50%;
  }

  #about_txt2 {
    padding: 4rem 1rem 1rem 0.5rem;
    font-size: 1rem;
    font-weight: lighter;
    text-indent: 20px;
    text-align: justify;
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








