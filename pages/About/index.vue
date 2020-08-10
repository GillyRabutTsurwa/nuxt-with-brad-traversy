<template>
  <div>
    <h1>About Dad Jokes</h1>
    <p>
      Voici une application qui affiche des bons dad jokes
    </p>
    <h4>Stopped @ 15:10</h4>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "À Propos",
      meta: [
        {
          hid: "description",
          name: "about-page",
          content: "about"
        }
      ]
    }
  }
}
</script>

<style>
</style>