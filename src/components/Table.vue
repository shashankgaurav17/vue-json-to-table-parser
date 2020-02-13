<template>
  <div class="table-view">
    <div
      v-for="(row, index) in iterateData(actualData)"
      :key="index"
      class="row-view m-2"
    >
      <div v-if="getRowValueType(actualData[row]) === 'object'" class="d-flex">
        <div class="key p-2 text-capitalize">{{ row }}</div>
        <div>
          <div
            v-for="(row2, index2) in iterateData(actualData[row])"
            :key="index2"
            class="row-view m-2"
          >
            <Row
              :type="getRowValueType(actualData[row][row2])"
              :rowKey="row2"
              :rowValue="actualData[row][row2]"
            />
          </div>
        </div>
      </div>
      <div v-else>
        <Row
          :type="getRowValueType(actualData[row])"
          :rowKey="row"
          :rowValue="actualData[row]"
        />
      </div>
    </div>
  </div>
</template>

<script>
import * as data from "@/config/data.json";
import Row from "@/components/Row";
export default {
  components: {
    Row
  },
  data() {
    return {
      actualData: data.default
    };
  },
  methods: {
    iterateData(object) {
      return Object.keys(object);
    },
    getRowValueType(val) {
      if (typeof val !== "object") {
        return typeof val;
      }
      return Array.isArray(val) ? "array" : "object";
    }
  }
};
</script>

<style scoped lang="scss">
.table-view {
  .row-view {
    border: 2px solid grey;
    border-radius: 2px;
  }
}

.key {
  background: lightblue;
}
</style>
