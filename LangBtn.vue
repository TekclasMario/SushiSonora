<template>
  <v-layout justify-end colum>
    <v-btn
      id="hey"
      round
      v-for="entry in languages"
      :key="entry.title"
      @click="changeLocale(entry.language)"
      medium
      v-bind:color="entry.color"
      class="white--text"
    >{{ entry.title }}</v-btn>
  </v-layout>
</template>

<script>
import i18n from "@/plugins/i18n";
export default {
  data() {
    return {
      languages: [
        { flag: "us", language: "en", title: "English", color: "#006847" },
        { flag: "es", language: "es", title: "Español", color: "#CE1126" }
      ]
    };
  },
  methods: {
    changeLocale(locale) {
      i18n.locale = locale;
    }
  }
};
</script>
