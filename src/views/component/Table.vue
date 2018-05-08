<template>
  <div class="main">
    <el-table
      :data="list"
      border
      align="center"
      stripe>
      <el-table-column
        type="index"
        label="序列"
        align="center"
        width="80">
      </el-table-column>
      <el-table-column
        prop="name"
        label="姓名"
        >
      </el-table-column>
      <el-table-column
        prop="gender"
        label="性别"
        >
        <template slot-scope="scope">
          <div :class="{'man': scope.row.gender === 1 , 'woman': scope.row.gender === 2}">{{differentColor(scope.row.gender)}}</div>
        </template>
      </el-table-column>
    </el-table>
  </div>
</template>

<style>
  .el-table .man {
    color: green;
  }
  .el-table .woman {
    color: red;
  }
</style>

<script>
export default {
  data() {
    return {
      list: [{
        name: 'Joel',
        gender: 1
      }, {
        name: 'Mary',
        gender: 2
      }, {
        name: 'Jimmy',
        gender: 3
      }],
    }  
  },
  methods: {
    differentColor(gender) {
      if(gender === 1) {
        return '男'
      }else if(gender === 2) {
        return '女'
      }else {
        return '未知'
      }
    }
  }
}
</script>

<style scoped></style>