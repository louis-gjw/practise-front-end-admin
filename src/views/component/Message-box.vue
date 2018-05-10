<template>
  <div class="main">
    <el-button type="danger" @click="open2">删除</el-button>
    <br>
    姓名: {{name}}
    <el-button :plain="true" @click="open3">录入姓名</el-button>

  </div>
</template>

<script>
export default {
  data() {
    return {
      name: '未设置'
    }  
  },
  methods: {
    open() {
      this.$alert('本网站基于 Vue 开发', {
        confirmButtonText: '确定',
        callback: action => {
          this.$message({
            type: 'info',
            message: `action: ${ action }`
          });
        }
      });
    },
    open2() {
      this.$confirm('确认删除?', {
        confirmButtonText: '确定',
        cancelButtonText: '取消',
        type: 'warning'
      }).then(() => {
        this.$message({
          type: 'success',
          message: '删除成功!'
        });
      }).catch(() => {
        this.$message({
          type: 'info',
          message: '已取消删除'
        });
      });
    },
    open3() {
      this.$prompt('请输入姓名', '提示', {
        confirmButtonText: '确定',
        cancelButtonText: '取消',
      }).then(({ value }) => {
        this.name = value
      }).catch(() => {
        
      });
    }
  },
  mounted() {
    this.open()
  }
}
</script>

<style scoped></style>