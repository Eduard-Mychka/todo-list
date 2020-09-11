<template>
  <div>
    <h2>Home page</h2>
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Animi culpa
      debitis, placeat illum dignissimos architecto quae necessitatibus possimus
      consequuntur facere quibusdam harum laboriosam unde cumque assumenda?
      Eaque ex magnam id.
    </p>
    <router-link class="todos" to="/todos">Todos</router-link>
  </div>
</template>

<style scoped>
p {
  color: rgb(183, 212, 255);
  letter-spacing: 1px;
}
.todos {
  color: rgb(0, 225, 255);
  font-size: 18px;
  letter-spacing: 1px;
}
</style>
