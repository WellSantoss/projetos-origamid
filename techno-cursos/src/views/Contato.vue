<template>
  <div>
    <div v-if="loading">
      <Loading />
    </div>
    <transition>
      <div v-if="api">
        <h1>Contato</h1>
      </div>
    </transition>
  </div>
</template>

<script>
import fetchData from "@/mixins/fetchData.js";

export default {
  name: "contato",
  mixins: [fetchData],
  created() {
    this.fetchData("/contato");
  },
};
</script>

<style></style>
