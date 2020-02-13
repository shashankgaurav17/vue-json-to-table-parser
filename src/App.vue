<template>
  <div id="app">
    <Table2 :data="data2" />
  </div>
</template>

<script>
import Table2 from "./components/Table2.vue";
import * as data2 from "@/config/data2.json";

export default {
  components: {
    Table2
  },
  data() {
    return {
      data2: data2.default
    };
  }
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.cursor-pointer {
  cursor: pointer;
}
</style>
