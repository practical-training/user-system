<template>
  <div class="tables">
    <el-table
      :data="tableData"
      style="width: 100%"
    >
      <el-table-column
        fixed
        type="selection"
        width="50"
      />
      <el-table-column
        fixed
        prop="name"
        label="姓名"
        width="100"
      />

      <el-table-column
        prop="province"
        label="所在机构"
        width="200"
      />
      <el-table-column
        prop="city"
        label="职务"
        width="100"
      />
      <el-table-column
        prop="address"
        label="执业年限"
        width="100"
      />
      <el-table-column
        prop="zip"
        label="手机号"
        width="120"
      />
      <el-table-column
        prop=""
        label="区域"
        width="140"
      />
      <el-table-column
        prop="a"
        label="邀请状态"
        width="140"
      />
      <el-table-column
        prop="b"
        label="邀请人"
        width="72"
      />
      <el-table-column
        prop=""
        label="邀请记录"
        width="180"
      />
      <el-table-column
        prop="c"
        label="Alpha用户"
        width="100"
      />
      <el-table-column
        prop="d"
        label="iCourt学员"
        width="100"
      /><el-table-column
        prop=""
        label="参加课程次数"
        width="120"
      />

      <el-table-column
        fixed="right"
        label="操作"
        width="210"
      >
        <template slot-scope="scope">
          <el-button type="text" size="small" @click="handleClick(scope.row)">查看</el-button>
          <el-button type="text" size="small" disabled>编辑</el-button>
          <el-button type="text" size="small" disabled>我的邀请</el-button>
        </template>
      </el-table-column>
    </el-table>
    <div class="block">
      <el-pagination
        :current-page="currentPage4"
        :page-sizes="[100, 200, 300, 400]"
        :page-size="100"
        layout="total, sizes, prev, pager, next, jumper"
        :total="400"
        @size-change="handleSizeChange"
        @current-change="handleCurrentChange"
      />
    </div>
  </div>

</template>
<script>
// import './css/table.css'
// import Data from '../../../../data/table.json'
export default {
  components: {

  },
  props: {

  },
  data() {
    return {
      tableData: [{
        name: '王小虎',
        province: '广州市法律援助处',
        city: '主任',
        address: '',
        a: 'A+ 联系企业家中',
        b: '王储00',
        c: '否',
        d: '否',
        zip: 16666666666

      }, {
        name: '王小虎',
        province: '广州市法律援助处',
        city: '主任',
        address: '',
        a: 'A+ 联系企业家中',
        b: '王储00',
        c: '否',
        d: '否',

        zip: 16666666666
      }, {
        name: '王小虎',
        province: '广州市法律援助处',
        city: '主任',
        address: '',
        a: 'A+ 联系企业家中',
        b: '王储00',
        c: '否',
        d: '否',
        zip: 16666666666
      }, {
        name: '王小虎',
        province: '广州市法律援助处',
        city: '主任',
        address: '',
        a: 'A+ 联系企业家中',
        b: '王储00',
        c: '否',
        d: '否',
        zip: 16666666666
      }]
      // tableList:Data
    }
  },
  computed: {

  },
  created() {
    // console.log(this.tableList.date.entities)
  },
  mounted() {

  },
  methods: {
    handleClick(row) {
      console.log(row)
    }
  }
}
</script>
<style scoped lang="">

</style>
