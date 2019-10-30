<template>
  <div>
    <Proxy :info="info" @change="handleProxyChange" />
  </div>
</template>

<script>
import Proxy from "./Proxy.vue";
export default {
  components: {
    Proxy
  },
  data: () => {
    return {
      info: {}
    };
  },
  methods: {
    handleProxyChange(val) {
      window.isUpdatingChildComponent = true;
      this.info.name = val;
      // this.info = { name: val };
    },
  }
};
</script>
