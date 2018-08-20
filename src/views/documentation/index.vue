<template>
  <div class="page" id="page" style="margin-bottom: 50px">
    <el-radio-group v-model="isCollapse"  style="margin-bottom: -20px;">
      <el-radio-button :label="false">用户管理</el-radio-button>
      <el-radio-button :label="true">用户字段</el-radio-button>
    </el-radio-group>
    <main>
      <div class="left">
        <el-menu
          class="el-menu-vertical-demo"
          background-color="#F0F0F0"
          active-text-color="#2893FF"
          style="width: 230px;text-align: left">
          <el-submenu index="1">
            <template slot="title">
              <i class="el-icon-news"></i>
              <span>鸿合科技信息部</span>
            </template>
          <el-submenu index="1-1" >
            <template slot="title">
              <i class="el-icon-news"></i>
              <span>鸿合科技-信息部</span>
            </template>
            <el-submenu index="1-1-1">

              <template slot="title">
                <i class="el-icon-news"></i>
                <span>鸿合科技信息部</span></template>
              <el-menu-item index="1-1-1-1"  @click="list(1)">flag</el-menu-item>
              <el-menu-item index="1-1-1-2" >123</el-menu-item>
            </el-submenu>
            <el-menu-item index="1-1-2">123</el-menu-item>
            <el-menu-item index="1-1-3">123</el-menu-item>
            <el-menu-item index="1-1-4">123</el-menu-item>
            <el-menu-item index="1-1-5">123</el-menu-item>
            <el-menu-item index="1-1-6">123</el-menu-item>
          </el-submenu>
<!--2-->
            <el-submenu index="1-2" >
              <template slot="title">
                <i class="el-icon-news"></i>
                <span>鸿合科技-信息部</span>
              </template>
              <el-submenu index="1-2-1">

                <template slot="title">
                  <i class="el-icon-news"></i>
                  <span>鸿合科技信息部</span></template>
                <el-menu-item index="1-2-1-1"  @click="list(1)">flag</el-menu-item>
                <el-menu-item index="1-2-1-2" >123</el-menu-item>
              </el-submenu>
              <el-menu-item index="1-2-2">123</el-menu-item>
              <el-menu-item index="1-2-3">123</el-menu-item>
              <el-menu-item index="1-2-4">123</el-menu-item>
              <el-menu-item index="1-2-5">123</el-menu-item>
              <el-menu-item index="1-2-6">123</el-menu-item>



            </el-submenu>



          </el-submenu>

        </el-menu>
      </div>
      <div class="right">
        <router-view></router-view>
      </div>
    </main>
  </div>
</template>
<script>
 // import {logout,getShopNotifyTotal} from '../../api/config'
  export default {
    name: 'Documentation',
    data() {
      return {
        numMessage: '0',
        isCollapse:false
      }
    },
    created() {
      this.getData()
    },
    methods: {
      getData() {
        /* var self = this;
        getShopNotifyTotal({status:'0'}).then(function (res1) {
          if ( res1.data.status == 0) {
            self.numMessage = res1.data.data
          }
        })*/
      },
      change() {
        this.$router.push("/pjManage")
      },
      list(act) {
        if(act==1){
          this.$router.push('/index1')
        }
        /* if(active1==2){
          this.$router.push('/shopPeizhi')
        }else if(active1!=2){
          this.$message({
            message: '您还没有认证申请店铺，请先申请',
            type: 'warning'
          })
          this.$router.push('/myrenzheng')
        }*/
    }
  }
}
</script>
<style scoped>
  .page{
    width: 100%;
    height: 100%;
    padding: 0;
    margin: 0;
  }
  main{
    margin: 20px 0 0 0;
    /* margin-top: 80px;
      margin-left: 0;
     margin-right: 0;*/

    width: 100%;
    height:100%;
    position: relative;
    left:0;
    float:left;
    /*left: -930px;*/
  }
  .left{
    width: 230px;
    min-height: 700px;
    height: 100%;
    border: 1px solid transparent;
    position: absolute!important;
    left: 0!important;
    top:0px;
    background-color: #F0F0F0;
  }
  .right{
    position: absolute;
    left: 240px;
    top: 0;
    right: 0;
    /* margin: 10px;*/
    height: 100%;
    padding:10px 50px 50px 50px;
    min-width: 800px;
    border: 1px solid transparent;
  }
  #page main .left .el-menu .el-menu-item.is-active{
    color: #f52648 !important;
  }
  #page main .left .el-menu .el-menu-item.disabledno1{
    color:black !important;
  }
</style>
<style>
  .el-button:hover .icon-yonghu{
    color:#d0d0d0;
  }
  .el-popover{
    text-align:center!important;
    min-width: 80px!important;
    background-color: #d0d0d0;/*#E0E0E0*/
  }
  #page main .left .el-menu .el-menu-item.disabledno1 i{
    color: black!important;
  }
  #page main .left .el-menu .el-menu-item.disabledno1 span{
    color: black!important;
  }
  #page main .left .el-menu .el-menu-item.is-active i{
    color: #f52648 ;
  }
  #page main .left .el-menu .el-menu-item.is-active span{
    color: #f52648;
  }

  .el-submenu .el-menu{
    padding-left: 13px;
  }
  .el-menu{
    overflow:hidden;
  }
</style>
