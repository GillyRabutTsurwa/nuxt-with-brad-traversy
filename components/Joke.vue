<template>
  <div class="joke">
    {{jokeProp}}
  </div>
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

.joke:hover {
  border: 1.5px solid #42b883;
}
</style>