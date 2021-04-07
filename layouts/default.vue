<template>
  <div>
    <nav class="navbar navbar-dark bg">
      <ul class="nav">
        <li class="nav-item ">
          <nuxt-link class="nav-link" to="/">Accueil</nuxt-link>
        </li>
        <li class="nav-item ">
          <nuxt-link class="nav-link" to="/ordered">Commandes</nuxt-link>
        </li>
      </ul>
    </nav>
    <!-- Container general -->
    <div class="container mt-3 pt-3">
      <Nuxt />
    </div>
  </div>
</template>

<!--Style Global-->
<style>
a {
  text-decoration: none;
  color: #7f8c8d;
}
a:hover {
  color: var(--greenHover);
}
.nuxt-link-exact-active {
  color: var(--green);
}
.bg {
  background-color: var(--greenDark);
}
</style>
