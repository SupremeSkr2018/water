<template>
  <div id="app">
    <div class="nav">
        <el-menu
          :default-active="activeIndex2"
          class="el-menu-demo"
          mode="horizontal"
          @select="handleSelect"
          background-color="#0e27bc"
          text-color="#fff"
          active-text-color="#ffd04b">
          <div class="title">上海市用水定额管理信息系统</div>
          <el-submenu index="1">
            <template slot="title">待处理事项</template>
            <el-menu-item index="1-1" @click="xingZheng()">行政审批事项</el-menu-item>
            <el-menu-item index="1-2">内部来函事项</el-menu-item>         
            </el-submenu>
          <el-submenu index="2">
            <template slot="title">用户管理</template>
            <el-menu-item index="2-1">开户</el-menu-item>
            <el-menu-item index="2-2">增自来水表</el-menu-item>
            <el-menu-item index="2-3">增回灌水水表</el-menu-item>
            <el-menu-item index="2-4">用户信息维护</el-menu-item>
            <el-menu-item index="2-5">水表信息维护</el-menu-item>
            <el-menu-item index="2-6">业务员调动</el-menu-item>
            <el-menu-item index="2-7">常规销表</el-menu-item>
            <el-menu-item index="2-8">常规销户</el-menu-item>
          </el-submenu>
          <el-submenu index="3">
            <template slot="title">定额管理</template>
            <el-menu-item index="3-1">定额参数配置</el-menu-item>
            <el-menu-item index="3-2">定额编制</el-menu-item>
            <el-menu-item index="3-3">定额下达</el-menu-item>
            <el-menu-item index="3-4">用户定额输入</el-menu-item>
          </el-submenu>
          <el-submenu index="4">
            <template slot="title">汇总开账</template>
            <el-menu-item index="4-1">导入供水企业数据</el-menu-item>
            <el-menu-item index="4-2">导出供水企业数据</el-menu-item>
            <el-menu-item index="4-3">提取考核表数据</el-menu-item>
            <el-menu-item index="4-4">抄表数据修改</el-menu-item>
            <el-menu-item index="4-5">汇总</el-menu-item>
            <el-menu-item index="4-6">执行情况计算</el-menu-item>
            <el-menu-item index="4-7">进入下一年月</el-menu-item>
          </el-submenu>
            <el-submenu index="5">
            <template slot="title">来函管理</template>
            <el-menu-item index="5-1">来函登记</el-menu-item>
            <el-menu-item index="5-2">来函查询</el-menu-item>
          </el-submenu>
            <el-submenu index="6">
            <template slot="title">查询统计</template>
            <el-menu-item index="6-1">全年情况查询</el-menu-item>
            <el-menu-item index="6-2">用户信息查询</el-menu-item>
            <el-menu-item index="6-3">定额查询</el-menu-item>
            <el-menu-item index="6-4">抄表信息查询</el-menu-item>
            <el-menu-item index="6-5">自来水公司数据查询</el-menu-item>
            <el-menu-item index="6-6">账务查询</el-menu-item>
          </el-submenu>
            <el-submenu index="7">
            <template slot="title">报表图表</template>
            <el-menu-item index="7-1">定额通知单</el-menu-item>
            <el-menu-item index="7-2">超定额通知单</el-menu-item>
            <el-menu-item index="7-3">报表打印</el-menu-item>
          </el-submenu>
        </el-menu>        
      </div>
      <xzsp v-show="isShow"></xzsp>
  </div>
</template>

<script>
import xzsp from '../components/xingZhengSP'
export default {
  components:{
    xzsp:xzsp
  },
  name: 'home',
  props: {
  
  },
    data() {
      return {
        activeIndex: '1',
        activeIndex2: '1',
        isShow:false
      };
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      },
      xingZheng(){
        this.isShow = true
      }
    }
}
</script>
<style lang="less" scoped>
  *{margin: 0 !important;}
  .title{
    color: white;
    font-size: 20px;
    display: inline-block;
    float: left;
    width: 25%;
    line-height: 57px;
  }
</style>