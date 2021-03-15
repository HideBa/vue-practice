<template>
  <div v-if="msg.length > 0">
    <p>{{msg}}</p>
  </div>
  <div v-else>no text here</div>
  <input type="text" v-model="msg"/>
  <button @click="clear()">click here</button>
  <Counter />
  <br/>
  
</template>

<script>
  import Counter from "./components/Counter";

export default {
  data() {
    return {
      msg: "Hello World",
    }
  },
  methods: {
    clear: function(){ this.msg = "" }
  },
  components: {
    Counter
  }
}
</script>
