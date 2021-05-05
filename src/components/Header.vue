<template>
  <div class="header">
    <h1>{{ title }}</h1>
    <Button text="Add Task" color="green" />
<!--    <Button text="Update Task" color="blue" />-->
<!--    <Button text="Delete Task" color="red" />-->
  </div>
</template>

<script>
import Button from './Button'

export default {
  name: "Header.vue",
  props: {
    title: String
  },
  components: {
    Button
  }
}
</script>

<style scoped>
  .header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
  }
</style>