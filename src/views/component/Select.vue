<template>
  <div class="main">
    选择水果(单选):
    <el-select v-model="value" placeholder="请选择">
      <el-option
        v-for="item in list"
        :key="item.value"
        :label="item.label"
        :value="item.value">
      </el-option>
    </el-select>

    选择水果(多选):
    <el-select v-model="value2" multiple placeholder="请选择">
      <el-option
        v-for="item in list"
        :key="item.value"
        :label="item.label"
        :value="item.value">
      </el-option>
    </el-select>
    
    用户数据(远程数据):
    <el-select v-model="value3" placeholder="请选择">
      <el-option
        v-for="item in remoteList"
        :key="item.value"
        :label="item.name"
        :value="item.value">
      </el-option>
    </el-select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: [{
        label: '苹果',
        value: 1,
      },{
        label: '梨',
        value: 2,
      },{
        label: '香蕉',
        value: 3,
      },{
        label: '荔枝',
        value: 4,
      }],
      value: '',
      value2: '',
      value3: '',
      remoteList: []
    }  
  },
  methods: {
    fetchRemoteList() {
      this.$http.get('https://jsonplaceholder.typicode.com/users').then(data => {
        debugger
        this.remoteList = data.data
        debugger
      })
    }
  },
  mounted() {
    this.fetchRemoteList()
  }
}
</script>

<style scoped></style>