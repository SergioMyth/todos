<template>
  <header>
    <h1>{{ headerTitle }}</h1>
    <Button
      v-show="homePage"
      @btn-click="$emit('toggle-add-task')"
      :text="showAddTask ? 'Close' : 'Add todo'"
      :color="showAddTask ? 'red' : 'blue'"
    />
  </header>
</template>

<script>
import Button from './Button'

export default {
  name: 'Header',
  props: {
    headerTitle: String,
    // default: "frumlegt nafn",
    showAddTask: Boolean,
  },
  components: {
    Button,
  },
  computed: {
    homePage() {
      if (this.$route.path === '/') {
        return true
      } else {
        return false
      }
    },
  },
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
