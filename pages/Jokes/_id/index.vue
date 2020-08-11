//TODO: Review route parametres. Stuff like $route.params.id. A bit fuzzy
<template>
  <div>
    <!-- {{$route.params.id}} -->
    {{currentJokeObj.joke}}
  </div>
</template>

<script>
import axios from "@nuxtjs/axios";
export default {
    data() {
        return {
            currentJokeObj: {}
        }
    },
     // NEW:
    async created() {
        try {
        // NOTEIMPORTANT: Faites attention à syntaxe peu differente pour utiliser axios avec Nuxt dessous.
            const response = await this.$axios.$get(`https://icanhazdadjoke.com/j/${this.$route.params.id}`, {
            headers: {
                Accept: "application/json"
            }
      });
        // console.log(response);
        // console.log(response.results);
        console.log(response);
        this.currentJokeObj = {...response}
        } catch (error) {
        console.warn(error);
    }
  },
}
</script>

<style>
</style>