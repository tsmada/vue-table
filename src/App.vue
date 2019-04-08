<template>
  <div id="app" slot-scope="{columns, tableData}">
    <Table slot="{columns, tableData}" :columns="columns" :tableData="tableData"/>
  </div>
</template>

<script>
import Vue from 'vue';
import Component from 'vue-class-component';
import Table from './components/Table';

@Component({
  components: {
    Table,
  },
})
export default class App extends Vue {
  columns = ['id', 'employment status', 'name'];
  tableData = [
    { id: 1, value: 'Employed', name: 'Adam' },
    { id: 2, value: 'Unemployed', name: 'Adam' },
    { id: 3, value: 'Unemployed', name: 'Adam' },
    { id: 4, value: 'Employed', name: 'Adam' },
    { id: 5, value: 'Employed', name: 'Adam' },
  ];
}
</script>

<style>
#app {
  font-family: 'Roboto', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
