<template>
  <div class="about">
    <div style="margin-bottom: 10px">
      <el-input v-model="input" placeholder="请输入内容" style="width: 200px;margin-right: 10px"></el-input>
      <el-button type="warning">Check</el-button>
      <el-button type="info">Reset</el-button>
      <el-button type="primary">Add</el-button>
    </div>
    <el-table
        :data="tableData" style="width: 100%;margin-bottom: 12px">
      <el-table-column prop="date"  label="日期"  width="180"></el-table-column>
      <el-table-column prop="name"  label="姓名"  width="180"></el-table-column>
      <el-table-column prop="address"  label="地址"></el-table-column>
      <el-table-column label="操作">
      <el-button type="primary">Update</el-button>
      <el-button type="danger">Delete</el-button>
      </el-table-column>
    </el-table>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="currentPage4"
          :page-sizes="[100, 200, 300, 400]"
          :page-size="10"
          layout="total, sizes, prev, pager, next, jumper"
          :total="400">
      </el-pagination>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tableData: [{
        date: '2016-05-02',
        name: '山田',
        address: '東京都渋谷区恵比寿南2丁目'
      }, {
        date: '2016-05-04',
        name: '荻田',
        address: '東京都世田谷区三軒茶屋2丁目'
      }, {
        date: '2016-05-01',
        name: '山本',
        address: '東京都杉並区高円寺北4丁目11番3号'
      }, {
        date: '2016-05-03',
        name: '奥野',
        address: '東京都新宿区西新宿3丁目'
      }]
    }
  }
}
</script>