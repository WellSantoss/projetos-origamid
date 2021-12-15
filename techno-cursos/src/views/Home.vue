<template>
  <div>
    <div v-if="loading">
      <Loading />
    </div>

    <transition>
      <div v-if="api" class="conteudo">
        <div>
          <h1>Sobre a {{ api.titulo }}</h1>
          <p>{{ api.descricao }}</p>

          <router-link tag="button" class="btn-cursos" to="/cursos"
            >Cursos</router-link
          >

          <div class="avaliacoes">
            <h2>Avaliações</h2>
            <ul>
              <li v-for="avaliacao in api.avaliacoes" :key="avaliacao.nome">
                <p>{{ avaliacao.nome }}</p>
                <p>{{ avaliacao.descricao }}</p>
              </li>
            </ul>
          </div>
        </div>

        <img src="@/assets/aprender.png" alt="Aprenda Web Design" />
      </div>
    </transition>
  </div>
</template>

<script>
import fetchData from "@/mixins/fetchData.js";

export default {
  name: "Home",
  mixins: [fetchData],
  created() {
    this.fetchData("/home");
  },
};
</script>

<style scoped>
.btn-cursos {
  border: none;
  background: #4b8;
  border-radius: 4px;
  color: #fff;
  cursor: pointer;
  box-shadow: 0 4px 2pc rgba(0, 0, 0, 0.1);
  padding: 15px 40px;
  font-size: 1rem;
  margin: 10px 0 40px;
  font-family: "Avenir", Helvetica, Arial, sans-serif;
}
</style>
