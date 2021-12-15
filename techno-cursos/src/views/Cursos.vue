<template>
  <div>
    <div v-if="loading">
      <Loading />
    </div>

    <transition>
      <div v-if="api">
        <h1>Cursos</h1>
      </div>
    </transition>
  </div>
</template>

<script>
import fetchData from "@/mixins/fetchData.js";

export default {
  name: "cursos",
  mixins: [fetchData],
  created() {
    this.fetchData("/cursos");
  },
};
</script>

<style></style>
