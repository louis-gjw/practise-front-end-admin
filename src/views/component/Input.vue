<template>
  <div class="main">
    <el-input v-model="input" placeholder="请输入内容"></el-input>
    <el-input
      type="textarea"
      :rows="2"
      placeholder="请输入内容"
      v-model="textarea">
    </el-input>
    <el-input-number v-model="num" :controls="false"></el-input-number>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input:'',
      textarea:'',
      num:1
    }  
  },
  methods: {
    
  }
}
</script>

<style scoped></style>