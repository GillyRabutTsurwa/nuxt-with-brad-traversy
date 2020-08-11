<template>
  <div class="jokes-container">
    <Joke v-for="currentJoke in jokes" v-bind:key="currentJoke.id" v-bind:jokeProp="currentJoke.joke" v-bind:idProp="currentJoke.id" />
  </div>
</template>

<script>
import axios from "@nuxtjs/axios";
import Joke from "../../components/Joke";
 
export default {
  components: {
    Joke: Joke
  },
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
        headers: {
          Accept: "application/json"
        }
      });
      // console.log(response);
      // console.log(response.results);
      let data = response.results;
      this.jokes = data;
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
.jokes-container {
  margin: 0 auto;
  text-align: center;
  width: 75%;
}
</style>