<script setup>
import { RouterLink, RouterView } from 'vue-router'



</script>

<template>
  <header class="header">
    <link rel="stylesheet" href="style.css">
    <section class="flex">
      <div class="icons" style="line-height: 40px;">
        <nav>
          <RouterLink to="/" style="text-decoration: none; color: black; font-size: 18px;">Home</RouterLink>
          <RouterLink to="/about" style="text-decoration: none; color: black; font-size: 18px;">About</RouterLink>
          <RouterLink to="/contact" style="text-decoration: none; color: black; font-size: 18px; ">Contact</RouterLink>
        </nav>
      </div>
  </section>
  </header>

  <RouterView />
</template>

<style scoped>

.header{
    background-color: white;
    position: relative;
    top:0; left: 0; right: 0;
    z-index: 1000;
    text-align: center;
}

.header .flex{
    padding: 30px 40px ;
    position: relative;
    display: flex;
    align-items:center;
    flex-wrap: wrap;
    justify-content: space-between;
}

nav a.router-link-exact-active {
  color: black;
  text-decoration: none;
}


nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid black;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(160px / 2);
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
