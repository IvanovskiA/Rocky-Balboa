<template>
  <header>
    <nav>
      <ul>
        <li><nuxt-link to="/" class="text">Home Page</nuxt-link></li>
        <li><nuxt-link to="/about" class="text">About Rocky</nuxt-link></li>
        <li><nuxt-link to="/characterRocky" class="text">Character biography</nuxt-link></li>
        <li><nuxt-link to="/rockyS" class="text">Rocky's series</nuxt-link></li>
        <li><nuxt-link to="/createdBy" class="text"><i>CreatedBy</i></nuxt-link></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
header {
  width: 100%;
  height: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: yellow;
}

.text{
  color: black;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

li {
  margin: 0 10px;
}

a {
  text-decoration: none;
  color: white;
}
</style>