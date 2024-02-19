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
      fetch('https://vovachegotov.amocrm.ru/api/v4/leads',{
        headers: {
          'Authorization: Bearer ': "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6ImI1NTQ2MGNiNzNlNjllNmI0MzIwMWRhZTIyN2ZkYThmNDY1MzNkZjc3YWYyOGExZThjNjEwOGE2NGFmMWEyZGQ3ZDhmMTEyNzJmZTY4ODQ3In0.eyJhdWQiOiI0ZmE3M2VhNi1jMDdlLTQ3OTEtODk4MC1iNzYxNjVmODkyMGMiLCJqdGkiOiJiNTU0NjBjYjczZTY5ZTZiNDMyMDFkYWUyMjdmZGE4ZjQ2NTMzZGY3N2FmMjhhMWU4YzYxMDhhNjRhZjFhMmRkN2Q4ZjExMjcyZmU2ODg0NyIsImlhdCI6MTcwODM1Njk5NiwibmJmIjoxNzA4MzU2OTk2LCJleHAiOjE3MDg0NDMzOTYsInN1YiI6IjEwNjc5NDk0IiwiZ3JhbnRfdHlwZSI6IiIsImFjY291bnRfaWQiOjMxNTcxODE0LCJiYXNlX2RvbWFpbiI6ImFtb2NybS5ydSIsInZlcnNpb24iOjIsInNjb3BlcyI6WyJwdXNoX25vdGlmaWNhdGlvbnMiLCJmaWxlcyIsImNybSIsImZpbGVzX2RlbGV0ZSIsIm5vdGlmaWNhdGlvbnMiXSwiaGFzaF91dWlkIjoiMWJmNWRlZGEtNzdmOS00YWJlLWJhMTQtOTVlMzRmZjdhYzVjIn0.o4QGpHohAOVtGMJdqwaKq8rFb_jTtT3VVjSmVyTjM4w0z-2WCwQzuc8tZiWzaJtUp0j5hGLu8fZqSJ_ao8LMub1yukBguSHKIEj1SaXCLwlLD6QNMiQcmGpGK202laC4mkidQf115n44-je_tyjXi_oTL71zKrOLvX0HGnQShkYtSh3SF00IPnOuuZb2y-yffQdSpaePBP-letfc00M4Q4u8RS3w-gSTBmEStPpkNAh1RphfIFY1ai2wApCCcizWLes7mV1IedN2CD97qlxs69CkHojaRfK_od9YUx_itEg8TuQwRaZDNWN2_G4AWpfcFMCUBTZZwq0b90zJtVxQvg"
        }
      })
      .then(response => response.json())
      .then(json => {console.log(json)})
      .catch(() => {
        alert('Server error')
      })
  }
}
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
