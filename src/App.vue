<template>
  <div v-if="msg.length > 0">
    <p>{{msg}}</p>
  </div>
  <div v-else>no text here</div>
  <input type="text" v-model="msg"/>
  <button @click="clear()">click here</button>
</template>

<script>

export default {
  data() {
    return {
      msg: "Hello World",
    }
  },
  methods: {
    clear: function(){ this.msg = "" }
  }
}
</script>
