<template>
  <div>
    <Event :name="name" @change="handleEventChange" />
  </div>
</template>

<script>
import Event from "./Event";
export default {
  components: {
    Event,
  },
  data() {
    return {
      name: "",
    };
  },
  methods: {
    handleEventChange(val, callback) {
      this.name = val;
      callback && callback("hello");
    }
  }
};
</script>
