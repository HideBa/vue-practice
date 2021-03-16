<template>
  <input
v-model="task.title" type="text" placeholder="Input your task here" />
  <!-- <div>{{ task.title }}</div>
  <input type="checkbox" v-model="task.isDone" /> -->
  <button @click="addNewTask">add</button>
</template>

<script>
export default {
  props: {
    addTask: Function,
  },
  data() {
    return {
      newTask: {
        title: "",
        // id: Math.floor(Math.random() * (100 - 1) + 1),
        isDone: false,
      },
    };
  },
  methods: {
    addNewTask: function() { 
      this.props.addTask(this.newTask)
    }
  }
};
</script>
