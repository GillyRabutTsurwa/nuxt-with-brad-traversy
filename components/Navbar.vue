<template>
  <nav class="navigation">
    <h2 class="navigation__logo">Dad Jokes</h2>
    <ul class="navigation__list">
      <li class="navigation__list--item">
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li class="navigation__list--item">
        <nuxt-link to="/about">About</nuxt-link>
      </li>
      <li class="navigation__list--item">
        <nuxt-link to="/jokes">Jokes</nuxt-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {

}
</script>

<style>
.navigation,
.navigation__list {
  display: flex;
}

.navigation__logo {
  letter-spacing: -2.5px;
  color: #fff;
  font-size: 2rem;
}

.navigation {
  justify-content: space-between;
  align-items: center;
  padding: 0 2rem;
  height: 9vh;
  background-color: #42b883;
}

.navigation__list {
  list-style-type: none;
}

.navigation__list--item {
  margin: 0 1rem;
}

.navigation__list--item a:link,
.navigation__list--item a:visited {
  color: #fff;
  text-decoration: none;
  font-weight: bold;
  font-size: 1.2rem;
}
</style>