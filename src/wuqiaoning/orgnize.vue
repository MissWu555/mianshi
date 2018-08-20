<template>
  <div class="page">
    <el-form :model="FormRe" :label-position="labelPosition" ref="FormRe1"  :rules="rules1"  label-width="150px" class="biaoDan" >
        <el-form-item label="公司名称:" prop="companyName">
          <el-input v-model="FormRe.companyName"></el-input>
        </el-form-item>

    </el-form>
  </div>
</template>
<script>
    export default {

        data() {
            return {}
        }
    }
</script>
<style scoped>

</style>
