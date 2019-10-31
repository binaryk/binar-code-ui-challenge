<template>
  <table class="table">
    <thead>
      <slot name="tableHeader">
        <th v-for="(column,index) in tableHeader" :key="index">{{ column }}</th>
      </slot>
    </thead>
    <tbody>
      <template>
        <tr v-for="(item,index) in data" :key="index">
          <slot :row="item">
            <td v-for="(column, index) in columns" :key="index">{{ item[column.toLowerCase()] }}</td>
          </slot>
        </tr>
      </template>
    </tbody>
  </table>
</template>
<script>

export default {
  name: "scoped-slot-table",
  props: {
    tableHeader: {
      type: Array,
      default: () => []
    },
    data: Array,
    columns: Array
  },
  created: function() {
    this.$eventHub.on('editRow',(data)=>{console.log("emmited",data)});

  },
  mounted() {
  },
  methods: {
    handleEvent() {
      console.log("event from parent");
    },
    hasValue(item, column) {
      return item[column.toLowerCase()] !== "undefined";
    },
    itemValue(item, column) {}
  }
};
</script>
<style scoped>
.table {
}

td,
th {
  padding: 10px;
}

tr:nth-child(even) {
}

tr:hover {
}

th {
}
</style>
