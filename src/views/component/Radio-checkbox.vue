<template>
  <div class="main">
    <el-radio class="radio" v-model="radio" label="1">备选项</el-radio>
    <el-radio class="radio" v-model="radio" label="2">备选项</el-radio>
    <el-checkbox-group v-model="checkList">
    <el-checkbox label="复选框 A"></el-checkbox>
    <el-checkbox label="复选框 B"></el-checkbox>
    <el-checkbox label="复选框 C"></el-checkbox>
  </el-checkbox-group>
  </div>
</template>

<script>
export default {
  data() {
    return {
      radio:null,
      checkList:[]
    }  
  },
  methods: {
    
  }
}
</script>

<style scoped></style>