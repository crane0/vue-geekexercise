<template>
  <div>
    name: {{ name || "--" }}
    <br />
    <input :value="name" @change="handleChange" />
    <br />
    <br />
    <div @click="handleDivClick">
      <button>重置成功</button>
      <button @click.stop>重置失败</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "EventDemo",
  props: {
    name: String
  },
  methods: {
    handleChange(e) {
      const res = this.$emit("change", e.target.value, val => {
        console.log('val', val);
      });
      console.log(res, res === this);
    },
    handleDivClick() {
      this.$emit("change", "");
    },
  }
};
</script>
