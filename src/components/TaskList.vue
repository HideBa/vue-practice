<template>
  <Task addTask="addTask" />
  <div
v-for="task in tasks" :key="task.id"
>
    <!-- <div>{{ task.title }}</div> -->
    <input type="checkbox" v-model="task.isDone" /> {{task.title}}
  </div>
  <div>{{ counter }}</div>
  <button @click="increment" >increment</button>
</template>

<script>
import Task from "./Task";
export default {
  components: {
    Task,
  },
  data() {
    return {
      tasks: [
        {
          title: "hoeg",
          id: 1,
          isDone: true
        },
        {
          title: "aa",
          id: 2,
          isDone: true
        },
        {
          title: "hohhg",
          id: 3,
          isDone: true
        }
      ],
      counter: 0
    };
  },
  methods: {
    addTask: function (task) {
      this.tasks.push(task);
    },
    increment: function() {
      this.counter ++;
    }
  },
};
</script>
