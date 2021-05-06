<template>
  <div class="header">
    <h1>{{ title }}</h1>
    <Button
        v-show="homePage"
        @btn-click="$emit('toggle-add-task')"
        :text="showAddTask ? 'Close' : 'Add Task'"
        :color="showAddTask ? 'red' : 'green'"
    />
  </div>
</template>

<script>
import Button from './Button'
import AddTask from './AddTask'

export default {
  name: "Header.vue",
  props: {
    title: String,
    showAddTask: Boolean,
  },
  components: {
    Button
  },
  computed: {
    homePage() {
      if (this.$route.path === '/') {
        return true
      } else {
        return false
      }
    }
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