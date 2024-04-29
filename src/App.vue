<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/cat.jpeg" width="125" height="125" />

    <div class="wrapper">
      <h1>Sulthon</h1>

      <nav>
        <button style="background-color: darkcyan;"><RouterLink to="/">Home</RouterLink></button>
      <button style="background-color: darkcyan;"><RouterLink to="/about">ToDolist</RouterLink></button>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
/* Warna-warna tambahan */
:root {
  --color-primary: #007bff; /* Warna utama */
  --color-text: #f4e9e9; /* Warna teks */
  --color-background: #f8f9fa; /* Warna latar belakang */
  --color-border: #ced4da; /* Warna border */
}

header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-primary); /* Warna teks aktif */
}

nav a.router-link-exact-active:hover {
  background-color: var(--color-primary); /* Warna latar belakang saat dihover */
  color: #fff; /* Warna teks saat dihover */
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
  color: var(--color-text); /* Warna teks */
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    font-family:'Times New Roman', Times, serif;
    color: aquamarine;
    font-size: 50px;
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
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
