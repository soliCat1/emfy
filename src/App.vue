<template>
  <div>
    <span>{{ deals }}</span>
    <span></span>
  </div>
</template>

<script>


export default {
  name: "App",
  mounted() {
    fetch("https://vovachegotov.amocrm.ru/api/v4/leads",{
      mode: 'no-cors',
      headers: {
        'Authorization: Bearer': "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6Ijk2NDFjNzNkYWFmOWQzZDdkODBjNDIwZDNlOGZhYzBhNTk0Y2M2OGFjOTY5ODBkOWE4NDMyZGE2OWMxNGEzMTMzNjUwMWUwNmM4ODcxOWQxIn0.eyJhdWQiOiI0ZmE3M2VhNi1jMDdlLTQ3OTEtODk4MC1iNzYxNjVmODkyMGMiLCJqdGkiOiI5NjQxYzczZGFhZjlkM2Q3ZDgwYzQyMGQzZThmYWMwYTU5NGNjNjhhYzk2OTgwZDlhODQzMmRhNjljMTRhMzEzMzY1MDFlMDZjODg3MTlkMSIsImlhdCI6MTcwODAyMjkwMCwibmJmIjoxNzA4MDIyOTAwLCJleHAiOjE3MDgxMDkzMDAsInN1YiI6IjEwNjc5NDk0IiwiZ3JhbnRfdHlwZSI6IiIsImFjY291bnRfaWQiOjMxNTcxODE0LCJiYXNlX2RvbWFpbiI6ImFtb2NybS5ydSIsInZlcnNpb24iOjIsInNjb3BlcyI6WyJwdXNoX25vdGlmaWNhdGlvbnMiLCJmaWxlcyIsImNybSIsImZpbGVzX2RlbGV0ZSIsIm5vdGlmaWNhdGlvbnMiXSwiaGFzaF91dWlkIjoiMzdiM2I3OGMtNTRkNi00ZjI1LWE4YjktZjQ2NTcwMWU0ZDYxIn0.IRIQRYWFS5iymKJz_n3ri3-qYIv2jZC5OCwO6JgFd_bnE3dvxpQIpEvpngkwPjEUWutnMrl8wLkgCduQxZwMDIHIVXM3mi7chWs0aNB2TvPIYyl8CjeY2xb2wbhkyA6AZVUAYix1idsbo9_CYwZ71hcHBuRNWgvQQQ4nB9cMdougc-8QjhkBFy6scx-aTva1zSnbJ6nDLV-xESUvxEjlrgX91av3wnO6mrmOsfiUTA14xu_9VTd6k-dEpvuPmRhzJ3DdZNsPXB_DZpyAj6AlusrNmlelzr8L_itHFUqiVjmx26AkuKyYSy4q5tYSzPRwQ-XaKc6kDCaPZLnXwNEoQQ" 
    }
      
    })
      .then((response) => response.json())
      .then((json) => {console.log(json),
      this.deals = json})
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
