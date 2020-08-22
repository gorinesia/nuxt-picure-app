<template>
  <header>
    <nav>
      <ul>
        <li><nuxt-link to="/">ラーメン</nuxt-link></li>
        <li><nuxt-link to="/recipes">寿司</nuxt-link></li>
        <li><nuxt-link to="/about">カバ</nuxt-link></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
header {
  width: 100%;
  height: 80px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: navy;
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
  font-weight: bold;
  margin: 5px 20px;
}

a {
  text-decoration: none;
  color: orange;
}
</style>