<template>
  <form @submit.prevent="onSubmit">
    <div class="input-group mb-3">
      <input
        type="text"
        class="form-control"
        v-model="title"
        placeholder="Write a comment"
        aria-label="Write a comment"
        aria-describedby="button-addon2"
      />
      <div class="input-group-append">
        <button
          class="btn btn-outline-secondary"
          type="submit"
          id="button-addon2"
        >
          Create
        </button>
      </div>
    </div>
  </form>
</template>

<script>
export default {
  data() {
    return {
      title: "",
    };
  },
  methods: {
    onSubmit() {
      if (this.title.trim()) {
        const newTodo = {
          id: Date.now(),
          title: this.title,
          completed: false,
        };
        this.$emit("add-todo", newTodo);
        this.title = "";
      }
    },
  },
};
</script>

<style scoped>
form {
  display: flex;
  width: 40%;
  margin-left: 2rem;
}

input {
  background-color: rgb(215, 250, 255);
  font-weight: 600;
}
</style>
