//TODO: Review route parametres. Stuff like $route.params.id. A bit fuzzy
<template>
  <div class="joke-id-container">
    <!-- {{$route.params.id}} -->
    <nuxt-link to="/jokes" class="back-2-jokes-btn button--grey">Back</nuxt-link>
    <p class="joke-text">
      <strong>{{currentJokeObj.joke}}</strong>
    </p>
    <figcaption>Joke: {{$route.params.id}}</figcaption>
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
     //TESTING: changing created to beforecreate
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
.joke-id-container {
  margin: 0 3rem;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}

.back-2-jokes-btn {
  align-self: flex-start;
  margin: 0;
}
.joke-text {
  font-size: 5rem;
}
</style>