<template>
  <div id="app">
    <span class="cursor-pointer" @click="type = 0">Table1</span>
    <span class="cursor-pointer" @click="type = 1">Table2</span>
    <Table v-if="type === 0" />
    <Table2 v-if="type === 1" :data="data2" />
  </div>
</template>

<script>
import Table from "./components/Table.vue";
import Table2 from "./components/Table2.vue";

import * as data2 from "@/config/data2.json";

export default {
  components: {
    Table,
    Table2
  },
  data() {
    return {
      type: 0,
      data2: data2.default
    }
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
