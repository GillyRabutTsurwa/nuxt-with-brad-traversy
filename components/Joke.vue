<template>
  <nuxt-link v-bind:to="`/jokes/${idProp}`">
    <div class="joke">
      {{jokeProp}}
    </div>
  </nuxt-link>
</template>

<script>
export default {
    props: {
        jokeProp: {
            type: String,
            required: true
        },
        idProp: {
            type: String,
            required: true
        }
    }
}
</script>

<style>
.joke {
  margin: 1rem 0;
  padding: 2rem 0;
  border: 0.3px solid lightgrey;
  cursor: pointer;
}

a:link,
a:visited {
  text-decoration: none;
  color: #34495e;
  font-weight: normal;
}

a:hover,
a:active {
  color: #34495e;
  font-weight: bold;
}

.joke:hover {
  border: 1.5px solid #42b883;
}
</style>