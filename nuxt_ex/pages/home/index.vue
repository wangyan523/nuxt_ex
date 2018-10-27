<template>
  <div class="home_box">
    <el-button type="text" @click="dialogVisible = true">{{homeData}}</el-button>
    <el-dialog
      title="提示"
      :visible.sync="dialogVisible"
      width="30%"
      :before-close="handleClose">
      <span>{{welcomeData}}</span>
      <span slot="footer" class="dialog-footer">
        <el-button @click="dialogVisible = false">取 消</el-button>
        <el-button type="primary" @click="dialogVisible = false">确 定</el-button>
      </span>
    </el-dialog>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      homeData: 'this is my home',
      welcomeData: 'welcom my home',
      dialogVisible: false,
    }
  },
  methods: {
    handleClose(done) {
        this.$confirm('确认关闭？')
          .then(_ => {
            done();
          })
          .catch(_ => {});
      }
  }
}
</script>

