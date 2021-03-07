<template>
  <div id="to-do-form">

    <form @submit.prevent="onSubmit()">
      <h2 class="label-wrapper">
        <label for="new-todo" class="label__lg">
          What needs to be done?
        </label>
      </h2>
      <input class="input__lg" v-model.trim="label" id="new-todo" type="text" name="new-todo" autocomplete="off">
      <button class="btn btn__primary btn__lg" type="submit" > Add</button>

    </form>
  </div>
</template>

<script>
export default {
  name: "ToDoForm",
  data() {
    return {
      label: ""
    }
  },
  methods: {
    onSubmit() {
      if (this.label === "") {
        return;
      }
      this.$emit('todo-added', this.label)
      this.label = ''
    }
  }
}
</script>

<style scoped>

</style>