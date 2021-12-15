<template>
  <header>
    <nav>
      <div class="logo">
        <router-link to="/">Techno</router-link>
      </div>
      <ul>
        <li><router-link to="/cursos">Cursos</router-link></li>
        <li><router-link to="/contato">Contato</router-link></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
header {
  background: #234;
}

nav {
  max-width: 800px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

header a {
  color: #fff;
}

ul li {
  display: inline-block;
}

li a {
  padding: 0 10px;
  margin-left: 20px;
}

.logo {
  padding: 20px;
}

.logo a {
  font-size: 1.2rem;
  color: #fff !important;
}

a.router-link-active {
  color: #4b8;
}
</style>
