<template>
  <li>
    <span v-bind:class="{ done: todo.completed }">
      <input type="checkbox" v-on:change="todo.completed = !todo.completed" />
      <strong>{{ index + 1 }}</strong>
      {{ todo.title | uppercase }}
    </span>
    <button class="close" v-on:click="$emit('remove-todo', todo.id)">
      &times;
    </button>
  </li>
</template>

<script>
export default {
  props: {
    todo: {
      type: Object,
      required: true,
    },
    index: Number,
  },
  filters: {
    uppercase(value) {
      return value.toUpperCase();
    },
  },
};
</script>

<style scoped>
li {
  /* border: 1px solid rgb(189, 189, 189); */
  display: flex;
  justify-content: space-between;
  padding: 0.5rem 2rem;
  margin-bottom: 1rem;
  color: black;
  letter-spacing: 1px;
}

.close {
  color: rgb(0, 0, 0);
  font-weight: bold;
  font-size: 2rem;
  outline: none;
}

input {
  margin-right: 1rem;
}

.done {
  text-decoration: line-through;
  color: rgb(0, 60, 83);
}
</style>
