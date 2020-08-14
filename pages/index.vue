// NOTEIMPORTANT: Voici le page domicile
<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        Dad Jokes App
      </h1>
      <div class="links">
        <a href="https://icanhazdadjoke.com/api" target="_blank" class="button--green">
          API Source
        </a>
        <a href="https://nuxtjs.org/guide" target="_blank" class="button--green">
          Nuxt Docs
        </a>
        <a href="https://github.com/GillyRabutTsurwa" target="_blank" class="button--grey">
          My GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Domicile",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Dad Jokes Home Page"
        }
      ]
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  /* min-height: 91vh; */
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
