<template>
  <div id="app">
    <img alt="Vue logo" width="120" src="./assets/logo.png" />
    <h2>Vue JS</h2>
    <hr />

    <router-view />
  </div>
</template>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 20px 60px 40px;
  background: rgb(107, 107, 107);
  background: linear-gradient(
    0deg,
    rgba(107, 107, 107, 1) 0%,
    rgba(255, 255, 255, 1) 100%
  );
  box-shadow: 0 14px 28px rgba(0, 0, 0, 0.25), 0 10px 10px rgba(0, 0, 0, 0.22);
}

h2 {
  letter-spacing: 3px;
}
</style>
