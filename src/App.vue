<script setup>
</script>
<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <div class="container-fluid">
        <router-link class="navbar-brand" to="/">
          <img src="./assets/pikachu.png" width="30" height="24" class="d-inline-block align-text-top">
          PokeDex
        </router-link>


        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
          aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <router-link class="nav-link" aria-current="page" to="/">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/about">About</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <div class="main">
      <router-view></router-view>
    </div>

    <footer class="bg-dark text-light">
      <div>
        <a href="https://github.com/Brunomelo0/PokeDex"><img src="./assets/github.svg" alt="Github link"></a>
      </div>
    </footer>
  </div>
</template>

<style>
body {
  height: 100vh;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: rgb(78, 153, 241);
  background: linear-gradient(90deg, rgba(78, 153, 241, 1) 0%, rgba(124, 177, 240, 1) 35%, rgba(238, 152, 190, 1) 100%);
}

footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 56px;
}

</style>