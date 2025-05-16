<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div class="layout">
    <header>
      <img alt="app logo" class="logo" src="@/assets/logo.png" width="125" height="125" />
      <div class="wrapper">
        <HelloWorld msg="Hamm" />
        <nav>
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/about">About</RouterLink>
          <RouterLink to="/inicio">Inicio</RouterLink>
        </nav>
      </div>
    </header>

    <main class="main-content">
      <RouterView />
    </main>
  </div>  
</template>

<style scoped>
.layout {
  display: flex;
  min-height: 100vh;
}

header {
  line-height: 1.5;
  max-height: 100vh;
  border-right: 1px solid var(--color-border);
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 15%;
  min-height: 100vh;
  padding: 2rem 1rem;
  position: fixed;
}

.logo {
  display: block;
  margin-bottom: 2rem;
}

nav {
  width: 100%;
  font-size: 1rem;
  text-align: left;
  margin-top: 2rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

nav a.router-link-exact-active {
  border-left: 0.25rem solid var(--color-border);
  background-color: var(--color-primary);
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;

}

.main-content {
  flex: 1;
  padding: 2rem;
  min-height: 100vh;
  margin-left: 15%;
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
