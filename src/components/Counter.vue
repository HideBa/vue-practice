<template>
  <div>Total:</div>
  <div>{{ total }}</div>
  <button @click="increment">increment</button>
  <button @click="decrement">decrement</button>
</template>

<script>
export default {
  data() {
    return {
      total: 0,
    };
  },
  methods: {
    increment: function () {
      this.total++;
    },
    decrement: function () {
      this.total = this.total - 1;
    },
  },
};
</script>
