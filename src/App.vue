<template>
  <div id="app">
    
  <el-container style="height:590px; border: 1px solid #eee">
        <el-aside width="200px" style="background-color: rgb(238, 241, 246)">
            <el-menu >
                <el-submenu index="1">
                    <template slot="title"><i class="el-icon-tickets"></i>角色权限</template>
                    <el-menu-item-group>
                        <template slot="title"></template>
                        <el-menu-item index="1-1">应用</el-menu-item>
                        <el-menu-item index="1-2">角色</el-menu-item>
                    </el-menu-item-group>

                </el-submenu>
                <el-submenu index="2">
                    <template slot="title"><i class="el-icon-menu"></i>组织架构</template>
                    <el-menu-item-group>

                        <el-menu-item index="2-1">部门</el-menu-item>
                        <el-menu-item index="2-2">员工</el-menu-item>
                    </el-menu-item-group>

                </el-submenu>
                <el-submenu index="3">
                    <template slot="title"><i class="el-icon-setting"></i>审批</template>
                    <el-menu-item-group>

                        <el-menu-item index="3-1">审批流程</el-menu-item>
                        <el-menu-item index="3-2">数据导出</el-menu-item>
                    </el-menu-item-group>
                    <el-menu-item-group title="假期">
                        <el-menu-item index="3-3">假期管理</el-menu-item>
                    </el-menu-item-group>

                </el-submenu>

                <el-submenu index="4">
                    <template slot="title"><i class="el-icon-date"></i>考勤</template>
                    <el-menu-item-group>

                        <el-menu-item index="4-1">考勤组设置</el-menu-item>

                    </el-menu-item-group>
                    <el-menu-item-group title="考勤统计">
                        <el-menu-item index="4-2">月度</el-menu-item>
                        <el-menu-item index="4-3">每日</el-menu-item>
                    </el-menu-item-group>

                </el-submenu>


            </el-menu>
        </el-aside>

      
<router-view>
</router-view>
    </el-container>




  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  }
}
</script>

<style>

.el-header {
    background-color: #B3C0D1;
    color: #333;
    line-height: 60px;
}

.el-aside {
    color: #333;
}
</style>
