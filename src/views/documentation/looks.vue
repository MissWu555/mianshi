<template>
  <div>
    <div style="width: 100%;text-align: left;padding-left: 20px">基本信息</div>
<el-form :model="FormRe" :label-position="left"  label-width="150px" >

  <el-form-item label="账号:" style="width: 450px" required>
    <el-input v-model="FormRe.a" auto-complete="off"></el-input>
  </el-form-item>
  <el-form-item label="用户名:" style="width: 450px" required>
    <el-input v-model="FormRe.b" auto-complete="off"></el-input>
  </el-form-item>
  <el-form-item label="密码:" style="width: 450px"  required>
    <el-input v-model="FormRe.c" auto-complete="off"></el-input>
  </el-form-item>
  <el-form-item label="手机号:"  style="width: 450px" >
    <el-input v-model="FormRe.d" auto-complete="off"></el-input>
  </el-form-item>
  <el-form-item label="邮箱:"  style="width: 450px" >
    <el-input v-model="FormRe.e" auto-complete="off"></el-input>
  </el-form-item>
  <el-form-item label="安全级别:"  style="width: 450px" >
    <el-input v-model="FormRe.f" auto-complete="off"></el-input>
  </el-form-item>
  <el-form-item label="直接上级:"  style="width: 450px" >
    <el-input v-model="FormRe.g" auto-complete="off"></el-input>
  </el-form-item>
</el-form>
    <p style="color: red">默认扩展字段</p>
    <hr />
    <el-form :model="FormRe" :label-position="left"  label-width="150px" >

      <el-form-item label="一级经理:" style="width: 450px" >
        <el-input v-model="FormRe.a" auto-complete="off"></el-input>
      </el-form-item>
      <el-form-item label="二级经理:" style="width: 450px" >
        <el-input v-model="FormRe.b" auto-complete="off"></el-input>
      </el-form-item>
      <el-form-item label="一级财务:" style="width: 450px">
        <el-input v-model="FormRe.c" auto-complete="off"></el-input>
      </el-form-item>
      <el-form-item label="二级财务:"  style="width: 450px" >
        <el-input v-model="FormRe.d" auto-complete="off"></el-input>
      </el-form-item>
      <el-form-item label="分支商务:"  style="width: 450px" >
        <el-input v-model="FormRe.e" auto-complete="off"></el-input>
      </el-form-item>
      <el-form-item label="销售团队:"  style="width: 450px" >
        <el-input v-model="FormRe.f" auto-complete="off"></el-input>
      </el-form-item>
    </el-form>
<div style="text-align: right;line-height: 50px;background-color: #f0f0f0;margin: 0;padding-right: 10px">
  <el-button type="info" @click.native="back" >×取消</el-button>
  <el-button type="primary"  @click.native="down">√确定</el-button>
</div>
  </div>
</template>
<script>
    export default {
      props:{
        editFormVisible:{

        }
      },
        data() {
            return {
              FormRe:{
                a:"",
                b:"",
                c:"",
                d:"",
                e:"",
                f:"",
                g:""
              }
            }
        },
      methods:{
          show(){

          },
        back(){
console.log(this.editFormVisible)
          this.editFormVisible.editFormVisible=false
        }
      }

    }
</script>
<style scoped>

</style>
