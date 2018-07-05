<template>
    <div>
      <hot-table :settings="settings"></hot-table>
    </div>
</template>

<script>
  import HotTable from "@handsontable/vue"
  import '@/assets/css/handsontable.full.css'
  export default {
    name: 'Index',
    components: {
      HotTable
    },
    data () {
      return {
        settings: {
          data: [
            ["111", "Tesla", "Volvo", "Toyota", "Honda"],
            ["2017", 10, 11, 12, 13],
            ["2018", 20, 11, 14, 13],
            ["2019", 30, 15, 12, 13]
          ],
          rowHeaders: true,
          colHeaders: true,
          manualColumnResize: true,
          manualRowResize: true,
          manualColumnMove: true,
          columnSorting: true,
          contextMenu: {   //自定义右键菜单，可汉化，默认布尔值
            items: {
              "row_above": {
                name:'上方插入一行'
              },
              "row_below": {
                name:'下方插入一行'
              },
              "col_left": {
                name:'左方插入列'
              },
              "col_right": {
                name:'右方插入列'
              },
              "hsep1": "---------", //提供分隔线
              "remove_row": {
                name: '删除行',
              },
              "remove_col": {
                name: '删除列',
              },
              "make_read_only": {
                name: '只读',
              },
              "borders": {
                name: '表格线',
              },
              "commentsAddEdit": {
                name: '添加备注',
              },
              "commentsRemove": {
                name: '取消备注',
              },
              "freeze_column": {
                name: '固定列',
              },
              "unfreeze_column": {
                name: '取消列固定',
              },
              "hsep2": "---------",
            }
          }
        }
      }
    }
  }
</script>

<style scoped>

</style>
