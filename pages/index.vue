<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        Bienvenue sur le premier projet Nuxt/Vue.js d'Amandine Delavoie
      </h1>
      <div class="links">
        <a
          href="https://github.com/amandine16"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          GitHub
        </a>
        <a
          href="https://www.linkedin.com/in/amandine-delavoie-582900161/"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          Linkedin
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 2.5em;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 2em;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
.button--grey,
.button--green {
  padding: 10px 15px;
  border-radius: 10px;
  color: var(--greenDark);
  margin: 0 10px;
}
.button--green {
  background: var(--green);
}
.button--grey {
  background: var(--greenDark);
  color: var(--green);
}
</style>
