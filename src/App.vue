<template>
  <div>
    <span></span>
    <span></span>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  mounted() {
    fetch("https://vovachegotov.amocrm.ru/api/v4/leads")
      .then((response) => response.json())
      .then((json) => {console.log(json)})
      .catch(() => {
        alert("Server error");
      });
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
