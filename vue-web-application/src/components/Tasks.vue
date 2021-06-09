<template>
  <div>
    <div :key="task.id" v-for="task in tasks">
      <Task @toggle-reminder="$emit('toggle-reminder', task.id)" @delete-task='$emit("deleteTask", task.id)' :task="task"/>
    </div>
  </div>
</template>

<script>
import Task from "./Task";
export default {
  name: 'Tasks',
  props: {
    tasks: Array,
  },
  components: {
    Task,
  }
}
</script>

<style lang="sass" scoped>

</style>