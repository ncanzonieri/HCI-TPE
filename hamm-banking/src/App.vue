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
      <div class="wrapper">
        
        <nav>
          <RouterLink to="/">Inicio</RouterLink>
          <RouterLink to="/history">Historial</RouterLink>
          <RouterLink to="/account">Cuenta</RouterLink>
          <RouterLink to="/investments">Inversiones</RouterLink>
          <RouterLink to="/cards">Tarjetas</RouterLink>
          <RouterLink to="/settings">Ajustes</RouterLink>
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

.wrapper {
  width: 100%;
}

h1.textLogo{
  font-family: 'Lily Script One';
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
}


.logo-container {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 2rem;
}

header {
  line-height: 1.5;
  max-height: 100vh;
  border-right: 1px solid var(--color-border);
  display: flex;
  flex-direction: column;
  width: 15%;
  min-height: 100vh;
  padding: 2rem 1rem;
  position: fixed;
}

.logo {
  height: 4rem;
  width: auto;
  margin-bottom: 0;
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
</style>
