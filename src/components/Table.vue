<template>
  <div>
    <table>
      <thead>
        <th
          v-for="column in columns"
          :key="column"
          :column="column"
        >{{column}}</th>
      </thead>
      <tbody>
        <tr
          v-for="row in tableData"
          :key="row.id"
          :row="row.name"
        >
          <td
            v-for="cell in row"
            :key="cell"
            :cell="cell"
          >{{cell}}
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  props: {
    columns: {
      type: Array,
      required: false,
    },
    tableData: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style>

</style>
