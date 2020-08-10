<template>
  <h4>This is another Page</h4>
</template>

<script>
import axios from "@nuxtjs/axios"
export default {
  data() {
    return {
      jokes: []
    }
  },
  // NEW:
  async created() {
    try {
      // NOTEIMPORTANT: Faites attention à syntaxe peu differente pour utiliser axios avec Nuxt dessous.
      const response = await this.$axios.$get("https://icanhazdadjoke.com/search", {
        // NOTE: On peux aussi mettre cet objet headers au-dessous de declaration axios et déclarer l'objet ici
        headers: {
          Accept: "application/json"
        }
      });
      console.log(response);
    } catch (error) {
      console.warn(error);
    }
  },
  head() {
    return {
      title: "Autre Page",
      meta: [
        {
          hid: "description",
          name: "another-page",
          content: "another page"
        }
      ]
    }
  }
}
</script>

<style>
</style>