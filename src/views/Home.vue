  <template>
  <el-container class="home">
    <el-header style="text-align: left; font-size: 12px">
      
      <el-row type="flex" class="row-bg">
        <el-col :span="12">
          <div class="grid-content bg-purple">


      <span>应用</span>

          </div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple-light">

<el-input placeholder="请输入内容"  clearable></el-input>

          </div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple">

 <el-button type="primary" icon="el-icon-search">搜索</el-button>
<el-button type="primary" icon="el-icon-edit" circle></el-button>
  
  <el-button type="danger" icon="el-icon-delete" circle></el-button>
          </div>
        </el-col>
      </el-row>
      
    </el-header>
    <el-main>
<el-table
    :data="tableData7.filter(data => !search || data.name.toLowerCase().includes(search.toLowerCase()))"
    style="width: 100%">
    <el-table-column
      label="日期"
      prop="date">
    </el-table-column>
    <el-table-column
      label="姓名"
      prop="name">
    </el-table-column>
    <el-table-column
      align="right">
      <template slot="header" slot-scope="scope">
        <el-input
          v-model="search"
          size="mini"
          placeholder="输入关键字搜索"/>
      </template>
      <template slot-scope="scope">
        <el-button
          size="mini"
          @click="handleEdit(scope.$index, scope.row)">修改</el-button>
        <el-button
          size="mini"
          type="danger"
          @click="handleDelete(scope.$index, scope.row)">删除</el-button>
      </template>
    </el-table-column>
  </el-table>

    </el-main>
  </el-container>
</template>

  <script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  components: {
    HelloWorld
  },
  
  data() {
      return {
        tableData7: [{
          date: '2016-05-02',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1518 弄'
        }, {
          date: '2016-05-04',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1517 弄'
        }, {
          date: '2016-05-01',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1519 弄'
        }, {
          date: '2016-05-03',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1516 弄'
        }],
        search: ''
      }
    },
    methods: {
      handleEdit(index, row) {
        console.log(index, row);
      },
      handleDelete(index, row) {
        console.log(index, row);
      }
    },

};
</script>
