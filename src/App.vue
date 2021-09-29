<template>

  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/Completed">Completed</router-link>
    </div>
    <router-view/>
  </div>
  
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
  
}
body{
     background: rgb(22,0,36);
background: linear-gradient(90deg, rgba(22,0,36,0.6894958667060574) 0%, rgba(148,8,194,0.5942577714679622) 15%, rgba(15,121,143,0.6474790599833684) 100%); 
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
