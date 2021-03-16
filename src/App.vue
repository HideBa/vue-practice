<template>
  <div v-if="msg.length > 0">
    <p>{{ msg }}</p>
  </div>
  <div v-else>no text here</div>
  <input
v-model="msg" type="text" />
  <button @click="clear()">click here</button>
  <Counter />
  <TaskList />
  <br>
</template>

<script>
import Counter from "./components/Counter";
import TaskList from "./components/TaskList";

export default {
  components: {
    Counter,
    TaskList,
  },
  data() {
    return {
      msg: "Hello World",
    };
  },
  methods: {
    clear: function () {
      this.msg = "";
    },
  },
};
</script>
