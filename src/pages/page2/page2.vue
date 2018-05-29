<template>

    <div class="page2-wrap">
      <h2>element ui样式重置 可以写入assets/css/_diy-elementui.scss下</h2>
      <el-button type="text" @click="dialogVisible = true">点击打开 Dialog</el-button>
      <el-dialog
        title="提示"
        :visible.sync="dialogVisible"
        width="30%">
        <span>这是一段信息</span>
        <span slot="footer" class="dialog-footer">
          <el-button @click="dialogVisible = false">取 消</el-button>
          <el-button type="primary" @click="dialogVisible = false">确 定</el-button>
        </span>
      </el-dialog>
      
      <div style="margin-top:30px;">
         <el-rate
        v-model="value2"
        :colors="['#99A9BF', '#F7BA2A', '#FF9900']">
        </el-rate>
      </div>
      
      <div style="margin-top:30px;">        
        <el-date-picker
          v-model="value1"
          type="datetime"
          placeholder="选择日期时间">
        </el-date-picker>
      </div>
      
    </div>

</template>

<script type="text/javascript">

  export default {
     name: 'page2',
     data() {
      return {
        dialogVisible: false,
         value1: '',
        value2:null
      };
    },
  }
</script>

<style lang="scss" scoped>
  @import "~assets/css/lib-variable";
  @import "~assets/css/lib-mixin";

  .page2-wrap{
     color:#000;
  }

</style>
