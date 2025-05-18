<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="layout">
    <header>
      <div class="logo-container">
        <img alt="Hamm Logo" class="logo" src="./assets/logo.png"/>
        <h1 class="textLogo">Hamm</h1>
      </div>
      <div class="tab">
        <nav>
          <RouterLink to="/">Inicio</RouterLink>
          <RouterLink to="/cards">Tarjetas</RouterLink>
          <RouterLink to="/history">Historial</RouterLink>
          <RouterLink to="/account">Cuenta</RouterLink>
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

.tab {
  width: 100%;
}

h1.textLogo{
  font-family: 'Lily Script One';
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
}


.logo-container {
  padding: 1.1rem 1rem 0;
  width: 100%;
  display: flex;
  margin-bottom: 2rem;
}

header {
  line-height: 1.5;
  height: 100vh;
  display: flex;
  flex-direction: column;
  width: 15%;
  position: fixed;
  background-color: white;
  border-right: 0.1rem solid #e2cbcb;
}

.logo {
  height: 4rem;
  width: auto;
  margin-left: 1rem;
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
  width: 100%;
  font-weight: bold;
  border-left: 0.25rem solid var(--color-border);
  background-color: var(--color-primary);
  color: #222;
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
  width: 100%;
}

nav a {
  width: 100%;
  display: block;
  padding: 0.5rem 1rem;
  font-weight: bold;

}

.main-content {
  flex: 1;
  min-height: 100vh;
  margin-left: 15%;
}
/*
@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .tab {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
    justify-content: flex-start;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
  */
</style>
