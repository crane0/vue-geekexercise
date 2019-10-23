<template>
  <div>
    <p>Reversed message1: "{{ reversedMessage1 }}"</p>
    <p>Reversed message2: "{{ reversedMessage2() }}"</p>
    <p>{{ now }}</p>
<<<<<<< HEAD
=======
    <!-- $forceUpdate()强制重新 render -->
>>>>>>> 6c34fe6436a46320f6573ec721cffb6b19e4ebb4
    <button @click="() => $forceUpdate()">forceUpdate</button>
    <br />
    <input v-model="message" />
  </div>
</template>
<script>
export default {
  data() {
    return {
      message: "hello vue"
    };
  },
  computed: {
    // 计算属性的 getter
    reversedMessage1: function() {
      console.log("执行reversedMessage1");
      return this.message
        .split("")
        .reverse()
        .join("");
    },
    now: function() {
      return Date.now();
    }
  },
  methods: {
    reversedMessage2: function() {
      console.log("执行reversedMessage2");
      return this.message
        .split("")
        .reverse()
        .join("");
    }
  }
};
</script>
