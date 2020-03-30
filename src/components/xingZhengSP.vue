<template>
 <div id="app">
  <div class="form_table">
    <table class="layui-table">
        <thead>
          <tr>
            <th>序号</th>
            <th>到期天数</th>
            <th>来函类型</th>
            <th>办理状态</th>
            <th>来函编号</th>
            <th>许可受理号</th>
            <th>用户号</th>
            <th>用户名</th>
            <th>操作</th>
          </tr> 
        </thead>
        <tbody>
          <tr>
            <td>1</td>
            <td>2</td>
            <td>月计划调整</td>
            <td>计财科</td>
            <td>32232045</td>
            <td>FGHJ54565123</td>
            <td>145412</td>
            <td>上海******有限公司</td>
            <td onclick="operation()">操作</td>
          </tr>
          <tr>
            <td>1</td>
            <td>2</td>
            <td>月计划调整</td>
            <td>计财科</td>
            <td>32232045</td>
            <td>FGHJ54565123</td>
            <td>145412</td>
            <td>上海******有限公司</td>
            <td onclick="operation()">操作</td>
          </tr>
          <tr>
            <td>1</td>
            <td>2</td>
            <td>月计划调整</td>
            <td>计财科</td>
            <td>32232045</td>
            <td>FGHJ54565123</td>
            <td>145412</td>
            <td>上海******有限公司</td>
            <td onclick="operation()">操作</td>
          </tr>
          <tr>
            <td>1</td>
            <td>2</td>
            <td>月计划调整</td>
            <td>计财科</td>
            <td>32232045</td>
            <td>FGHJ54565123</td>
            <td>145412</td>
            <td>上海******有限公司</td>
            <td onclick="operation()">操作</td>
          </tr>
        </tbody>
    </table>
  </div>
   <div class="form_detail" style="display: none;">
      <div class="detail_left">
        <div>
          <table class="layui-table">
            <thead>
              <tr>
                <th>登记文号</th>
                <th>用户名</th>
                <th>用户号</th>
              </tr> 
            </thead>
            <tbody>
              <tr>
                <td>贤心</td>
                <td>92645266654</td>
                <td>777777777777</td>
              </tr>
              <tr>
                <td>许闲心</td>
                <td>132465888</td>
                <td>656666666666666</td>
              </tr>
            </tbody>
          </table>
        </div>
        <div style="margin-bottom: 20px;">
          <div style="height: 30px;line-height: 35px;background:#eaeaea;padding-left: 30px;">来函内容</div>
          <div style="height: 200px;border:1px solid #d8d8d8"></div>
        </div>
      </div>
      <div class="detail_right">
        <div style="margin-bottom: 20px;border:1px solid #d8d8d8;padding: 20px;">
          <div style="margin-bottom: 5px;">
            <span style="width: 146px;">用户名：</span> <input type="text">
            <span>行政许可受理编号：</span><input type="text">
            <span>统一审批编码：</span><input type="text">
          </div>
          <div style="margin-bottom: 5px;">
            <span style="width: 149px;">受理日期：</span><input type="text">
            <span>业务员：</span><input type="text">
            <input type="checkbox" style="margin-right: 10px;width: auto;"><span style="width: 50px;">托收</span>
            <input type="checkbox" style="margin-right: 10px;width: auto;"><span>承诺收费</span>           
          </div>
          <div style="margin-bottom: 5px;">
            <span>上月实用：</span><input type="text">
            <span>上月超定额量：</span><input type="text">           
          </div>
          <div style="margin-bottom: 5px;">
            <span>定额：</span><input type="text">
            <span>基建量：</span><input type="text">           
          </div>
          <div style="margin-bottom: 5px;">
            <span>超定额量：</span><input type="text">
            <span>超定额金额：</span><input type="text">                    
          </div>
          <div style="margin-bottom: 5px;">
            <div style="height: 30px;line-height: 35px;background:#eaeaea;padding-left: 30px;">调整后</div>
            <div>
              <span>超定额量：</span><input type="text">
              <span>超定额金额：</span><input type="text">                        
            </div>
          </div>
          <div>
            <div style="height: 30px;line-height: 35px;background:#eaeaea;padding-left: 30px;">合计</div>
            <div>
              <span>超定额金额：</span><input type="text">
              <span>调整后超定额金额：</span><input type="text">                        
            </div>
          </div>
          <div style="border-top: 1px solid #d8d8d8;margin-top: 10px;padding-top: 10px;">
            <p><span style="margin-bottom: 5px;">用户申请量：</span><input type="text"></p>
        </div>
          <div style="border-top: 1px solid #d8d8d8;margin-top: 10px;padding-top: 10px;">
              <p><span style="margin-bottom: 5px;">承办人建议量：</span><input type="text"></p>
              <p><span style="width: 146px;position: relative;bottom: 50px;">承办人意见：</span> <textarea name="" id="" cols="30" rows="10" style="width: 350px;height: 65px;resize: none;padding: 3px;"></textarea></p>         
          </div>
    </div>
      </div>
      <div style="clear: both;float: right;margin-bottom: 20px;">
        <button class="layui-btn" style="float: left;position: relative;right: 1000px;background: #1f5eff;" onclick="goBack()">返回待处理</button>
        <button class="layui-btn" style="float: right;position: relative;right: 60px;background: #1f5eff;">修改</button>
        <button class="layui-btn" style="float: right;position: relative;right: 55px;background: #1f5eff;">确认</button>
      </div>
      <div style="clear: both;float: right;">
        <button class="layui-btn" style="float: right;position: relative;right: 50px;background: #1f5eff;">文件列表</button>        
        <button class="layui-btn" style="float: right;position: relative;right: 55px;background: #1f5eff;">用水/收费情况</button>
        <button class="layui-btn" style="float: right;position: relative;right: 50px;background: #1f5eff;">提交</button>
      </div>  
   </div>     
</div> 
</template>
<script>
export default {
  name: 'xingZhengSP',
  props: {

  },
    data() {
      return {
        activeIndex: '1',
        activeIndex2: '1'
      };
    },
    methods: {

    }
}
</script>
<style lang="less" scoped>
  *{margin: 0 !important;}

</style>