<template>
  <h4>This is another Page</h4>
</template>

<script>
export default {
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