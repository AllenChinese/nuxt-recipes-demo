<template>
  <header>
    <nav>
      <ul>
        <li><nuxt-link to="/">Starting Page</nuxt-link></li>
        <li><nuxt-link to="/recipes">Recipes</nuxt-link></li>
        <li><nuxt-link to="/About">About</nuxt-link></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
header {
  display: flex;
  width: 100%;
  padding: 10px 0;
  margin: 0;
  justify-content: center;
  align-items: center;
  background-color: #521751;
}

ul {
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
  padding: 0;
  margin: 0;
}

li {
  margin: 0 10px;
}

a {
  text-decoration: none;
  color: #999;
}

.nuxt-link-exact-active.nuxt-link-active {
  color: #fff;
}
</style>

