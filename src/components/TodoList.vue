<template>
  <div>
    <p>Completed tasks: {{todos.filter(todo => {return todo.done === true}).length}}</p>
    <p>Pending: {{todos.filter(todo => {return todo.done === false}).length}}</p>
    <todo v-for="todo in todos" v-bind:todo="todo"></todo>
  </div>
</template>

<script type="text/javascript">
  import Todo from './Todo'

  export default {
    props: ['todos'],
    components: {
      Todo
    }
  }
</script>

<style>
</style>
