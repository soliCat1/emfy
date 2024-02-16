<template>
  <div>
    <span>{{ deals }}</span>
    <span></span>
  </div>
</template>

<script>

export default {
  name: "App",
  data: () => ({
    deals: []
  }),
  mounted() {
    fetch("https://vovachegotov.amocrm.ru/api/v4/leads")
      .then((response) => response.json())
      .then((json) => {console.log(json),
      this.deals = json})
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
