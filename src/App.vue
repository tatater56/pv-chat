<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style>
#app {
  margin: auto;
  width: 90%;
  max-width: 600px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  font-size: 100%;
}

.header {
  font-size: 2.5rem;
  font-weight: bold;
  margin-bottom: 20px;
}

.subheader {
  font-size: 1.6rem;
  font-weight: bold;
  margin: 0.2rem;
}

input {
  font-size: 1.8rem;
}
</style>
