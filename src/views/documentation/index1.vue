<template>
  <div class="ddList">
    <el-form  style="text-align: left;margin-top: 10px">
      <el-form-item>
        <el-button  @click.native="newtime" >+新建用户</el-button>
      </el-form-item>
    </el-form>
    <el-form :inline="true" style="text-align: right;margin-top: 10px">
      <el-form-item label="订单号:">
        <el-input v-model="goodshao" style="width:150px"></el-input>
      </el-form-item>
      <el-form-item>
        <el-button type="danger" @click.native="souSuo" >查询</el-button>
      </el-form-item>
      <el-form-item>
        <el-button type="success" :disabled="this.sels.length===0" @click.native="down">批量导入</el-button>
      </el-form-item>
    </el-form>
    <el-table :data="tableData" height="250" class="xuankuang"  border   @selection-change="handleSelectionChange">
      <el-table-column type="selection" width="120px">
      </el-table-column>
      <el-table-column  label="账号" prop="date">
      </el-table-column>
      <el-table-column label="姓名" prop="name" width="100px" >
      </el-table-column>
      <el-table-column  label="分部" show-overflow-tooltip min-width="100px" prop="address">
      </el-table-column>
      <el-table-column  label="部门" min-width="100px" prop="rote">
      </el-table-column>
      <el-table-column  label="状态锁定" prop="state">
      </el-table-column>
      <el-table-column label="启用状态" show-overflow-tooltip min-width="120px" prop="use">
        <!--<template slot-scope="scope">{{ scope.row.orderNumber}}</template>-->
      </el-table-column>
      <el-table-column  label="安全级别" prop="safe">
      </el-table-column>
    </el-table>
    <el-col :span="24" class="toolbar" style="margin-top: 20px">
      <el-pagination  layout="prev, pager, next, jumper" @current-change="handlePageChange" :page-size="pagesize" :total="total"
                      style="float:right;">
        {{this.page}}
      </el-pagination>
    </el-col>


    <el-dialog style="" title="添加新用户" width="900px" :visible.sync="b.editFormVisible" :close-on-click-modal="false">
      <ImpressReview  ref="UA" :editFormVisible="b"  ></ImpressReview><!--@updateList="updateList"-->
    </el-dialog>


  </div>
</template>
<script>
  import ImpressReview from './looks.vue'
  function H() {
    return {
      //查看
      editFormVisible: false,
    }
  }
    export default {
        data() {
            return {
              sels: [],
              tableData:[{
                date: '3333',
                name: '3323',
                address: '鸿合科技-信息部',
                rote:'信息部',
                state:'正常',
                use:'启用',
                safe:'0'

              },
                {
                  date: '2222',
                  name: '3323',
                  address: '鸿合科技-信息部',
                  rote:'信息部',
                  state:'正常',
                  use:'启用',
                  safe:'0'

                },
                {
                  date: '111',
                  name: '3323',
                  address: '鸿合科技-信息部',
                  rote:'信息部',
                  state:'正常',
                  use:'启用',
                  safe:'0'

                },
                {
                  date: '000',
                  name: '3323',
                  address: '鸿合科技-信息部',
                  rote:'信息部',
                  state:'正常',
                  use:'启用',
                  safe:'0'

                },
                {
                  date: '555',
                  name: '3323',
                  address: '鸿合科技-信息部',
                  rote:'信息部',
                  state:'正常',
                  use:'启用',
                  safe:'0'

                },
                {
                  date: '777',
                  name: '3323',
                  address: '鸿合科技-信息部',
                  rote:'信息部',
                  state:'正常',
                  use:'启用',
                  safe:'0'

                }
              ],
              page: 1,
              pagesize: 2,
              total: 0,
              b:H(),

            }
        },
      components:{
        ImpressReview
      },
    methods:{
          newtime(){
            this.b.editFormVisible=true
            var self=this;
            /*self.updateId0=row*/
            setTimeout(function () {
              self.$refs.UA.show();
            })
          },
      souSuo(){

      },
      //表格头部
      handleSelectionChange(sels) {
        this.sels = sels;
      },
      down(){

      },
      //分页下标
      handlePageChange(val){
        this.page = val;
       // this.getData();
      },
    }
    }
</script>
<style scoped>

</style>
