<template>
  <div class="main">
    <el-switch
      v-model="value"
      on-text="开"
      off-text="关"
      on-value="1"
      off-value="0">
    </el-switch>
  </div>
</template>

<script>
export default {
  data() {
    return {
      value: ''
    }  
  },
  methods: {
    
  }
}
</script>

<style scoped></style>