<template>
  <div class="regist_box">
    <el-button type="warning" @click="btnClick">{{btnData}}</el-button>
  </div>
</template>

<script>
export default {
  name: 'Regist',
  data() {
    return {
      btnData: '点我呀'
    }
  },
  methods: {
    btnClick() {
      console.log('点到了')
    }
  }
}
</script>

<style lang="less" scoped>

</style>


