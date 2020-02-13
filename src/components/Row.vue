<template>
  <div class="row-data">
    <div
      v-if="['string', 'number'].includes(type)"
      class="type-primitive d-flex"
    >
      <span class="key p-2 text-capitalize">{{ keyTitle }}</span>
      <span class="value p-2">{{ rowValue }}</span>
    </div>
    <div v-else-if="type === 'array'" class="type-primitive d-flex">
      <span class="key p-2 text-capitalize">{{ keyTitle }}</span>
      <div class="value p-2 d-inline-block">
        <div v-for="(val, index) in rowValue" :key="index">- {{ val }}</div>
      </div>
    </div>
    <!-- <div v-else>
      <Row type="string" :rowKey="keyTitle" :rowValue="rowValue" />
    </div> -->
    <!-- <div v-else class="type-object d-flex">
      <span class="key p-2 text-capitalize">{{ keyTitle }}</span>
      <pre class="d-inline-block p-2">{{ rowValue }}</pre>
    </div> -->
  </div>
</template>

<script>
// import Row from "@/components/Row";
export default {
  // name: "Row",
  // components: {
  //   Row
  // },
  props: {
    type: {
      type: String
    },
    rowKey: {
      type: String
    },
    rowValue: {
      type: [String, Number, Object, Array]
    }
  },
  computed: {
    keyTitle() {
      return this.rowKey.split("_").join(" ");
    }
  }
};
</script>

<style lang="scss" scoped>
.row-data {
}

.key {
  background: lightblue;
}
</style>
